// ROBB - ILUMINIZE / DIE ANDER

on
off
move_to_color				colorwheel
							  args:
							    - 16711
							    - 3145
							    - 0
							    - 0
							    - 0
							  params:
							    color_x: 16711
							    color_y: 3145
							
							
move_to_color_temp			knop in midde van colorwheel - Wit toon
								args[0] = color_temp_mireds 
							
step_with_on_off			= Brightness
								args[0] = (1 = down | 0 = up)
								
move_hue 					= oause / play button
								args[0] = geeft steeds 1 na 0 dan weer 1

move_to_color				= W+ knop  (kleur opties)
								args[0] = color_x
								args[1] = color_y
								
recall						= scene knoppen
								args[1] = scene number



// DE LANGE WITTE

step_with_on_off 			= in/decrease brightness	data.args[0] = 1 = decrease || data.args[0] = 0 = increase
move_with_on_off			= Long press brightness 	data.args[0] = 1 = decrease || data.args[0] = 0 = increase
stop_with_on_off			= Long press brightness	button release

recall 						= scene 			sceneUD = data.args[1]
store						= Long press of scene button data.args[1] = sceneID 


move_to_hue_and_saturation 	= color wheel 		data.args[0] = hue (0-254)		data.args[1]  = saturation (254)
move_to_color_temp			= whiteness bar		data.args[0] color_temp_mireds	(148 - 480)



on							= Need to say more?
off							= Need to say more?
