# HTML Controlled Mini Tank Rover 
For my Bluestamp Engineering project, I decided to make a Mini Tank Rover. The base project was very easy: assemble the main frame using unclear instructions, attach the motors to the back wheels, and connect the motors to the Arduino R3 Board using H-bridges so that one could control the movement of the rover when the Arduino was plugged into the computer. Once I was done with this part, I could modify the rover as much as I wanted. Thus, I decided to add a Raspberry Pi with a Picamera and a phone battery so that I could control the rover from far away, view its surroundings, and let it run without needing to have it plugged into an outlet. I even made the Picamera footage stream to an HTML website where I could also control the direction the rover was moving.

You should comment out all portions of your portfolio that you have not completed yet, as well as any instructions:
```HTML 
<!--- This is an HTML comment in Markdown -->
<!--- Anything between these symbols will not render on the published site -->
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Luna S. | Hunter College High School | Mechanical Engineering | Incoming Sophomore

**Replace the BlueStamp logo below with an image of yourself and your completed project. Follow the guide [here](https://tomcam.github.io/least-github-pages/adding-images-github-pages-site.html) if you need help.**

![Headstone Image](logo.svg)
  
# Final Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/F7M7imOVGug" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


For my third milestone, I got the buttons to work so that I could control the rover’s movements and stream the picamera footage from the same HTML website. In the code for the HTML website in Thonny, I added an onclick sendCommand function to each button so that when I pressed a button, the VNC viewer would tell the Arduino to make the rover move in a specific direction. However, I ran into trouble because I couldn’t get the rover to stop. Rather than create a stop button, I decided to make the default setting for the rover to stop. I wanted the buttons going in different directions would overwrite the stop command and make the rover move, but the moment I stopped pressing on the buttons, for the rover to stop moving. It didn't work out as intended because I didn’t know what to write for stop to become the default setting. Eventually, I added a onmouseleave sendCommand(‘Stop’) after the onclick sendCommand for each button so that the moment the mouse stopped hovering over the button, the rover would stop. Now, I had working buttons on my HTML website and I could make my rover move and stop whenever I wanted. My phone battery had also arrived so I was able to get the rover working without having to keep it plugged into an outlet. 

In the future, I might add a laser pointed to the rover for my cat to chase around. Overall, this was a really fun project and I learned a lot about HTML and Raspberry Pis since I had never worked with either in the past. I'm so happy that I finally completeted my rover and I can't wait to terrorize my cat with it!


# Second Milestone

**Don't forget to replace the text below with the embedding for your milestone video. Go to Youtube, click Share -> Embed, and copy and paste the code to replace what's below.**

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

For my second milestone, I incorporated a Raspberry Pi into my project. In order to be able to give the Arduino Board directions wirelessly from my computer, I needed a Raspberry Pi to act as a bridge between my computer and Arduino Board. The Raspberry Pi, which connected to my computer via the internet, would easily be able to receive directions from my computer wirelessly. So, I set up my Raspberry Pi and plugged it into the Arduino Board, making sure they could communicate between themselves. I coded for the Raspberry Pi using Thonny in VNC Viewer and connected it to the Arduino IDE. Pretty soon, I was able to send an instruction on which direction to move into my Raspberry Pi which would pass that on to the Arduino IDE and my mini tank rover would move in the desired direction. However, the Raspberry Pi still had to be plugged into an outlet for power and this energy would end up powering my entire rover. My phone battery hasn’t arrived yet, but once it does, I hope to be able to power the Raspberry Pi and rover with it. 
	
 I also set up a Picamera2 so that I would be able to view my rover’s surroundings in order to control the rover’s movements from far away. I sourced code from the internet to be able to stream the camera footage on an HTML website. I even added buttons for forward, left, right, and backward on the website, but they do not work yet. For my third milestone, I would like to get the buttons working so that I can control the rover from a single server instead of going back and forth between the VNC Viewer and an HTML website.
 

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/watch?v=xffqFFISyRU&list=PLe-u_DjFx7eticgHvdNBMS-CTTohSGwUM&index=51" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


  For my first milestone, I began by building my chassis by screwing 2 motors onto the back of the frame and attaching the back wheels to those motors. I then attached the front wheels to the frame by passing a screw through the hole and securing them to the side of my main frame using nuts. I then attached the treads to both wheels. Though the original tread was 50 pieces long, I removed six pieces from each tread to make two treads with 44 pieces. Once I could control the movement of the car, I would be able to move the car forward and backwards by using the back wheels to move the front wheels. 
	
 After building the car, I attached the H-bridge to the motors using the wires that came attached to the motors and screwed them into the H-bridge. I then used dupont wires to attach the H-bridge to my Arduino R3 Board so that I could control the movement of the motors and power them. For this, I coded what is shown below in Arduino IDE. AIA and AIB stood for Input A and B for Motor A (the motor on the right wheel) and BIA and BIB stood for Input A and B for Motor B (the motor on the left wheel). I made AIA and BIA move to make the car go backwards and AIB and BIB to make the car move forwards. To go right, I had the right wheel go backwards and the left wheel go forward and vice versa to move the car to the left. 
	
 With this, I was able to make my car go forwards, backwards, left, and right when the Arduino was plugged into my computer and using my computer as a power source. Though I could not spontaneously change the direction of the rover, it was able to follow a set of directions in the Arduino IDE and loop through the commands of moving forward for 3 seconds, backwards for 3 seconds, right for 3 seconds, and left for 3 seconds. 
  
  However, this was when I ran into my first problem. The front wheels would unscrew themselves as they ran and were not parallel to the main frame, preventing the rover from going straight. I solved this problem by adding 2 more nuts to the screw so that the nuts would unscrew more slowly. Though the nuts would still unscrew themselves with time, the car ran much more smoothly. In order to fully fix the problem, I would have needed a new set of wheels and another frame. Another issue I encountered was that even after I had uploaded the code from the Arduino IDE to the Arduino R3 Board and used a 9V battery for a power source, the rover would not be able to move in more than one direction and would stall after just a few seconds. My instructor and I attributed this problem to the rover being too heavy so we decided to remove the treads. This did make the rover move for a much longer period of time. However, only 3V of the 5V from the battery were making it to the wheels and the car would eventually stall after 1 minute without being able to go in multiple directions. Believing a repressor was limiting the capabilities of the Arduino, I replaced the motors. However, this changed nothing so we ordered a phone battery, which would be much more powerful than a 9V battery, to use for my second milestone to see whether that would make a difference.


# Schematics 
Here's where you'll put images of your schematics. [Tinkercad](https://www.tinkercad.com/blog/official-guide-to-tinkercad-circuits) and [Fritzing](https://fritzing.org/learning/) are both great resoruces to create professional schematic diagrams, though BSE recommends Tinkercad becuase it can be done easily and for free in the browser. 

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Tank Chassis Kit | Main Build | $20.99 | <a href = "https://www.amazon.com/TT02-Platform-Intelligent-Programmable-Educational/dp/B09V7T97RV/ref=sr_1_47?crid=OXLYH16H0GCU&dib=eyJ2IjoiMSJ9.IM0-vS-C-EGGeZYPYXycjiXnG-UaAN6F61k0uty1Gf7Zvh0napnIRqRGXq1IuD22hytT-vmhd517ZuEX4QTx0YLj-6Xg1qHbgq3-vFyBcnlffdq2mZMUjN7AM_enxzh168BCgy0heilUD6DuBDiMzeHFkUTl1EjzQ98hOqhX5u24U1Nehqhf7Ot1z9d6AcONjE8dUF-8R9fZHt91E9R1Q-m4MhMf5zKtI3DnhkOBo5FZ5KPHlLhPEG_bODR0o3NHvJ0jqsxNEJQuowLBlAuiZgpOM8AC42cBm014iuePsQg.xYj8I09trrOmQtlIo38ceHxknzHL5CnbhTfQMkfImSA&dib_tag=se&keywords=tank%2Brobot%2Barduino&qid=1718756297&sprefix=tank%2Brobot%2Barduino%2Caps%2C106&sr=8-47&th=1/" > Link </a> |
| UNO R3 Board | Told the Motors Which Direction to Spin In | $16.99 | <a href = "https://www.amazon.com/ELEGOO-Board-ATmega328P-ATMEGA16U2-Compliant/dp/B01EWOE0UU/ref=sr_1_2_sspa?crid=3A6NCD2X9JEMJ&dib=eyJ2IjoiMSJ9.AcWZy-Yg4mDTnhzEHozxzPZdVC5-KUL2tW-OQewDKpBB4brSpD-p4bn74WcXiW3KarYertgpNaLJ0VHKx0qsPqolKAhiz1GRG5BwJQl73cEvrlXIXNmqlpSvU7uu2aRVSwAZi9Gj2AjSPLM3esW1Gzy9xEiQ9oiR5LCNjh4MlYDx5mTm5sI4rsD4CFTipJnF572qXlickl35FRcCj8oMXQotumgqI4yEIq0HobOtIlEnNhtVB51JMBHhqtmmF_PC9WeHJ4ySUVVcv_gq3_VeG1aAEbdm4NXmmT6NOYPw4Qo.1PFdgFT22oqO5Mg6-6j_aUL_EV8tUPuaFrB5N9oaEX0&dib_tag=se&keywords=elegoo+arduino&qid=1716856465&s=electronics&sprefix=elegoo+arduino%2Celectronics%2C99&sr=1-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1/" > Link </a> |
| Electronics Kit | Didn't end up using this | $15.99 | <a href = "https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6](https://www.amazon.com/dp/B09YRJQRFF?psc=1&smid=A2WWHQ25ENKVJ1&ref_=chk_typ_imgToDp/" > Link </a> |
| Motor 8-pack | Turned the Back Wheels | $10.99 | <a href = "https://www.amazon.com/AEDIKO-Motor-Gearbox-200RPM-Ratio/dp/B09N6NXP4H/ref=sr_1_4?crid=1JP29NIWBLH2M&dib=eyJ2IjoiMSJ9.Wq3jKgOLbqtEP772vMD4pV5f-w3PLBdEpKqguykXOb0JFO14f4Dq0m_VDVUMUFtR8WFINUEticI3GXcoGqwXPqK9yIh04PhCktgccMz9zAUiKXMJPwmOTUp_6av3XuFD0lXo9WngN9iKI6YgZrhEEs9qnqbcB1GnvgntCdKz8Q1dFuNu61NgSE6Z8vBk3FRpaNcr1lCI7FApTiNi0Qce8gbfmMn6oUggZQHpIOKKZ6s.M7WsZ_ZZtm3rm93kKgw0NOxt1McVBYX6m55oGxu1xxI&dib_tag=se&keywords=dc+motor+with+gearbox&qid=1715911706&sprefix=dc+motor+with+gearbox%2Caps%2C126&sr=8-4/" > Link </a> |
| H-Bridge 5-pack | Connected Motors to Arduino R3 Board | $7.79 | <a href = "https://www.amazon.com/gp/product/B00M0F243E/ref=sw_img_1?smid=A30QSGOJR8LMXA&psc=1/" > Link </a> |
| Digital Multimeter | Checked if the Arduino R3 Board Received Power | $12.99 | <a href = "https://www.amazon.com/AstroAI-Digital-Multimeter-Voltage-Tester/dp/B01ISAMUA6/ref=sxin_17_pa_sp_search_thematic_sspa?content-id=amzn1.sym.e8da13fc-7baf-46c3-926a-e7e8f63a520b%3Aamzn1.sym.e8da13fc-7baf-46c3-926a-e7e8f63a520b&cv_ct_cx=digital+multimeter&dib=eyJ2IjoiMSJ9.5LQumrfBR8l0mKnJCJlRg73dxpou0gqYD_ffU3srgs0Utegwth8GcQCSVXVzeZeLSJx5J3itz5TLdmJHsrVITQ.-00jRPoT-bBy26YC4LzQ-S4cYdztgmSMGb83_WEm6HY&dib_tag=se&keywords=digital+multimeter&pd_rd_i=B01ISAMUA6&pd_rd_r=e1ff2570-7e4a-4906-bc55-6f819d48d1bc&pd_rd_w=h7HgL&pd_rd_wg=0ZcFH&pf_rd_p=e8da13fc-7baf-46c3-926a-e7e8f63a520b&pf_rd_r=R6YKX3NXTDQ1PQP4H8RM&qid=1715911879&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sr=1-1-7efdef4d-9875-47e1-927f-8c2c1c47ed49-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9zZWFyY2hfdGhlbWF0aWM&psc=1/" > Link </a> |
| 9V Batttery Clip Snap DC Plug 5-pack | I didn't end up using them | $5.99 | <a href = "https://www.amazon.com/5pack-Battery-2-1mm-Arduino-Corpco/dp/B01AXIEDX8/ref=sr_1_1?crid=1JMB76PI0E2LI&dib=eyJ2IjoiMSJ9.IxZhvVZzjl3mQ3hiFiq1KUOMvd6aWLHUvR5GaRVLvnLpCADw7ptUhm2ZbswcLA3OH-Srpw2qShEwZO-p10V1B08qcOrt0gncPdblQgSH8a_6PHpQ4-_vInA0lzCwWExsJlLpqvGmmsfJvBWkzMQwK15XFLF91dW2yPDl3lBPwRh1puqCFY1goDEn2acNaXvnhlfi_zHFc0AIek0u-9jV-YAmlN9oJPKaoz-6CPWMNs8_wBzmKTDVV8sra3clevWH3BHfH5dBOAWjjR5Fr-MvPr5f6THNw3WOMLeeKYAuS2E.8BHZWnq0i61MogcAFoJqxvFR64QYbjBONOTda2bvQE4&dib_tag=se&keywords=9v+battery+to+barrel&qid=1718991115&s=electronics&sprefix=9v+battery+to+barrel%2Celectronics%2C86&sr=1-1/" > Link </a> |
| 9V Battery 10-pack | I didn't end up using them either | $8.88 | <a href = "https://www.amazon.com/PKCELL-Maximum-Long-Lasting-Leak-Proof-Detectors/dp/B00ZTS55Y4/ref=sr_1_6_pp?crid=2K0AJR427U9BZ&dib=eyJ2IjoiMSJ9.kIe_PMQCi4Ug6zlF5WZlV8oIc-Y-uaSBWvVSgRZvU4gj5O2gnpiwdNWoMvEYGhF_AxjOUq-tL4vQTpozlHvH80-gRYK7-WjgiDMrFcuJCke-jQQN-hDGEerJ6OhTsJNE4eoWlpGNgyfTAAjSiEdQlppXTti2uSKFHx_nu2yrbVUMt8K2FabF9oVZxzDDhGJ-LumsKhLfnLsIxYFiFtiWDpNBkRhTCDHstSJy2fb8A8fzLz9DmP23Q2l3YaZl3LEZJkfggRkvzOXUB6h361b1kL9pZ2T7t14p_jKPf__qKbc.RZAhZjK7Pd3i56SIdCgUvvuqYeb76ipK_9xZ5qukj7U&dib_tag=se&keywords=9v+batteries&qid=1719014435&sprefix=9v+batteries%2Caps%2C117&sr=8-6/" > Link </a> |
| Raspberry Pi Kit | Receives Input from the Computer | $119.99 | <a href = "https://www.amazon.com/Vemico-Raspberry-Starter-Heatsinks-Screwdriver/dp/B09QGZ94M8/ref=sr_1_20?crid=3EO43F1FEOV0O&dib=eyJ2IjoiMSJ9.ualQ11OTmi8CjjOvKHbGSeoxaNIDkPpfJZtZyzHol1FvvEglqiwyyx0fx51TZiZ1aBaberSc_J42HaMFrKc4G4wzNZJZEEpXeUe5uPFLGOfeZg1JiJOFIRBWErdjcMSJmt9OiXh3fiaEklJDqjCH8YliLFrOMz2gDd9N61tXfyLELptXi2DxstQVgqAxXv9vJnZG8mc1uPn3ogYVtajj4NEvfs_J7KSsaUplZk2LAkNdh8C7VZAVCj9KGMicav_2LQeL3moiJ-zNLr78csIQdysoo0AdWn9HClXObBEGA2A.R84P9iUHYtjBbieyHy8tFMnaqBUBiYhKHI1MA9uJP1A&dib_tag=se&keywords=raspberry%2Bpi%2Bkit&qid=1716420057&s=electronics&sprefix=raspberry%2Bpi%2Bki%2Celectronics%2C105&sr=1-20&th=1/" > Link </a> |
| Picamera2 | Camera | $8.99 | <a href = "https://www.amazon.com/gp/product/B07RWCGX5K/ref=ox_sc_act_title_1?smid=A2IAB2RW3LLT8D&th=1/" > Link </a> |
| Phone Battery | Powers the Rover | $17.99 | <a href = "https://www.amazon.com/SIXTHGU-Portable-Charger-Charging-Flashlight/dp/B0C7PHKKNK/ref=sr_1_2_sspa?crid=2ZZM4AAZMMWHQ&dib=eyJ2IjoiMSJ9.W2Zx5_I3mKOn6UpwAzOw6PD0PNh1iaMRBiedequdv9weeWL0HPyPcxJBR9h6-LiFW-sHKnHSApN0sUxx0Q9xIRs80R57IlvvCsmEzXcktogo-4nP-NxrEZOy5dJTcXY8N-PBwfGt4fl_9LP8npenzDUV9TPA8KN6DMu175g6JegC_gZhAJrbqX94EfpQhLwP9vIJH45w2N-AFrfZZOy9jqk55gzVyk4Qst8uZvqn768.KBrc5_SqZ4e8zCpoFc-1C7rk02t3o2ykgDPB65W5JJU&dib_tag=se&keywords=always%2Bon%2Bpower%2Bbank&qid=1715957917&sprefix=always%2Bon%2Bpower%2Bbank%2Caps%2C107&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1/" > Link </a> |

# Other Resources/Examples

- [Picamera2 Streaming Source Code]([https://trashytuber.github.io/YimingJiaBlueStamp/](https://randomnerdtutorials.com/raspberry-pi-mjpeg-streaming-web-server-picamera2/))
