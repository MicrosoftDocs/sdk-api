---
UID: NF:directmanipulation.IDirectManipulationAutoScrollBehavior.SetConfiguration
title: IDirectManipulationAutoScrollBehavior::SetConfiguration
author: windows-sdk-content
description: Performs the auto-scroll animation for the viewport this behavior is attached to.
old-location: directmanipulation\idirectmanipulationautoscrollbehavior_setconfiguration.htm
tech.root: directmanipulation
ms.assetid: 2DE988EA-8690-4AF2-A545-8226032D6E83
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDirectManipulationAutoScrollBehavior interface [Direct Manipulation],SetConfiguration method, IDirectManipulationAutoScrollBehavior.SetConfiguration, IDirectManipulationAutoScrollBehavior::SetConfiguration, SetConfiguration, SetConfiguration method [Direct Manipulation], SetConfiguration method [Direct Manipulation],IDirectManipulationAutoScrollBehavior interface, directmanipulation.idirectmanipulationautoscrollbehavior_setconfiguration, directmanipulation/IDirectManipulationAutoScrollBehavior::SetConfiguration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationAutoScrollBehavior.SetConfiguration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationAutoScrollBehavior::SetConfiguration


## -description


Performs the auto-scroll animation for the viewport this behavior is attached to. 


## -parameters




### -param motionTypes [in]

A combination of <b>DIRECTMANIPULATION_MOTION_TRANSLATEX</b> and <b>DIRECTMANIPULATION_MOTION_TRANSLATEY</b> from <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a>. <b>DIRECTMANIPULATION_MOTION_NONE</b> cannot be specified.


### -param scrollMotion [in]

One of the values from <a href="https://msdn.microsoft.com/1184DD40-D615-440F-8B87-D53A475F8313">DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION</a>. 


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<b>SetConfiguration</b> takes effect immediately. If the content is not in inertia, and <b>DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION_STOP</b> is specified for <i>scrollMotion</i>, then this method returns S_FALSE. 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>spAutoScrollBehavior-&gt;SetConfiguration(DIRECTMANIPULATION_MOTION_TRANSLATEX, DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION_FORWARD));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6E847EE2-231C-4B09-955A-F546CC790E3C">IDirectManipulationAutoScrollBehavior</a>
 

 

