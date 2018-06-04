---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# D2D1_BLEND_MODE enumeration


## -description


The blend mode used for the <a href="https://msdn.microsoft.com/39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE">Blend effect</a>.


## -enum-fields




### -field D2D1_BLEND_MODE_MULTIPLY

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a mutiply effect." src="images/blend_mode_multiply_1.png"/>

### -field D2D1_BLEND_MODE_SCREEN

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a screen effect." src="images/blend_mode_screen_1.png"/>

### -field D2D1_BLEND_MODE_DARKEN

Basic blend formula for alpha only.  

<img alt="mathematical formula for a darken effect." src="images/blend_mode_darken_1.png"/>

### -field D2D1_BLEND_MODE_LIGHTEN

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a lighten effect." src="images/blend_mode_lighten_1.png"/>

### -field D2D1_BLEND_MODE_DISSOLVE

Given:
            

<ul>
<li>A scene coordinate XY for the current pixel</li>
<li>A deterministic pseudo-random number generator rand(XY) based on seed coordinate XY, with unbiased distribution of values from [0, 1]</li>
</ul>
<img alt="Mathematical formula for a dissolve blend effect." src="images/blend_mode_dissolve_1.png"/>


### -field D2D1_BLEND_MODE_COLOR_BURN

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) =  

<img alt="Mathematical formula for a coor burn effect." src="images/blend_mode_colorburn_1.png"/>

### -field D2D1_BLEND_MODE_LINEAR_BURN

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) =  

<img alt="Mathematical formula for a linear burn effect." src="images/blend_mode_linearburn_1.png"/>

### -field D2D1_BLEND_MODE_DARKER_COLOR

Basic blend formula for alpha only. 

<img alt="Mathematical formla for a darken color effect." src="images/blend_mode_darkencolor_1.png"/>

### -field D2D1_BLEND_MODE_LIGHTER_COLOR

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a lighter color effect." src="images/blend_mode_lightercolor_1.png"/>

### -field D2D1_BLEND_MODE_COLOR_DODGE

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) =  

<img alt="Mathematical formula for a color dodge effect." src="images/blend_mode_colordodge_1.png"/>

### -field D2D1_BLEND_MODE_LINEAR_DODGE

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a linear dodge effect." src="images/blend_mode_lineardodge_1.png"/>

### -field D2D1_BLEND_MODE_OVERLAY

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for an overlay effect." src="images/blend_mode_overlay_1.png"/>

### -field D2D1_BLEND_MODE_SOFT_LIGHT

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a soft light effect." src="images/blend_mode_softlight_1.png"/>

### -field D2D1_BLEND_MODE_HARD_LIGHT

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a hard light effect." src="images/blend_mode_hardlight_1.png"/>

### -field D2D1_BLEND_MODE_VIVID_LIGHT

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a vivid light effect." src="images/blend_mode_vividlight_1.png"/>

### -field D2D1_BLEND_MODE_LINEAR_LIGHT

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a linear light effect." src="images/blend_mode_linearlight_1.png"/>

### -field D2D1_BLEND_MODE_PIN_LIGHT

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a pin light effect." src="images/blend_mode_pinlight_1.png"/>

### -field D2D1_BLEND_MODE_HARD_MIX

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = 

<img alt="Mathematical formula for a hard mix effect." src="images/blend_mode_hardmix_1.png"/>

### -field D2D1_BLEND_MODE_DIFFERENCE

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>)


### -field D2D1_BLEND_MODE_EXCLUSION

Basic blend formulas with <i>f</i>(F<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub> – 2 * F<sub>RGB</sub> * B<sub>RGB</sub>


### -field D2D1_BLEND_MODE_HUE

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a hue blend effect." src="images/blend_mode_hue_1.png"/>

### -field D2D1_BLEND_MODE_SATURATION

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a sturation blend effect." src="images/blend_mode_saturation_1.png"/>

### -field D2D1_BLEND_MODE_COLOR

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a color blend effect." src="images/blend_mode_color_1.png"/>

### -field D2D1_BLEND_MODE_LUMINOSITY

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a luminosity blend effect." src="images/blend_mode_luminosity_1.png"/>

### -field D2D1_BLEND_MODE_SUBTRACT

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a subtract blend effect." src="images/blend_mode_subtract_1.png"/>

### -field D2D1_BLEND_MODE_DIVISION

Basic blend formula for alpha only. 

<img alt="Mathematical formula for a division blend effect." src="images/blend_mode_division_1.png"/>

### -field D2D1_BLEND_MODE_FORCE_DWORD



