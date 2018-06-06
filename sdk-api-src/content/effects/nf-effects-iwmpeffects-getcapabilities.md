---
UID: NF:effects.IWMPEffects.GetCapabilities
title: IWMPEffects::GetCapabilities
author: windows-sdk-content
description: The GetCapabilities method gets the capabilities of the visualization.
old-location: wmp\iwmpeffects_getcapabilities.htm
old-project: WMP
ms.assetid: e2efb0cd-417f-4b96-a4d7-c02c41a6244d
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: EffectsGetCapabilities, GetCapabilities, GetCapabilities method [Windows Media Player], GetCapabilities method [Windows Media Player],IWMPEffects interface, IWMPEffects interface [Windows Media Player],GetCapabilities method, IWMPEffects.GetCapabilities, IWMPEffects::GetCapabilities, effects/IWMPEffects::GetCapabilities, wmp.iwmpeffects_getcapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: effects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player version 7.0 or later
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - effects.h
api_name:
 - IWMPEffects.GetCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IWMPEffects::GetCapabilities


## -description



The <b>GetCapabilities</b> method gets the capabilities of the visualization.




## -parameters




### -param pdwCapabilities [out]

<b>DWORD</b> containing the capabilities.

The current values are as follows.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>EFFECT_CANGOFULLSCREEN</b> = 0x00000001;</td>
<td>The visualization is capable of full-screen rendering.</td>
</tr>
<tr>
<td><b>EFFECT_HASPROPERTYPAGE</b> = 0x00000002;</td>
<td>The visualization has a property page.</td>
</tr>
<tr>
<td><b>EFFECT_VARIABLEFREQSTEP</b> = 0x00000004;</td>
<td>The visualization will use frequency data with variable size steps. If this bit is set, step size is based on the media sampling frequency divided by BUFFER_SIZE. If this bit is not set and media is played that was sampled at a low frequency, the upper cells will be empty. For example, if an 8KHz sampled file is played and this bit is not set, the upper half of the frequency array (from 8KHz to 22KHz) will be empty. If this bit is set and an 8Khz sampled file is played, the frequency array will range from 20Hz to 8KHz in BUFFER_SIZE steps.</td>
</tr>
<tr>
<td><b>EFFECT_WINDOWED_ONLY</b> = 0x00000008</td>
<td>The visualization only renders in windowed mode.</td>
</tr>
<tr>
<td><b>EFFECT2_FULLSCREENEXCLUSIVE</b> = 0x00000010</td>
<td>The visualization uses exclusive mode when rendering full-screen. The Player will not resize the window to fill the screen. The visualization must create a top level window and handle resolution switching.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



A default implementation of this method is not included in the visualization wizard.




## -see-also




<a href="https://msdn.microsoft.com/0f2a6bda-3e1f-4509-b8ff-ccf0909aa9ba">IWMPEffects Interface</a>
 

 

