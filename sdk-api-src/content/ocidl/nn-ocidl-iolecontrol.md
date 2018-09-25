---
UID: NN:ocidl.IOleControl
title: IOleControl
author: windows-sdk-content
description: Provides the features for supporting keyboard mnemonics, ambient properties, and events in control objects.
old-location: com\iolecontrol.htm
tech.root: com
ms.assetid: ef85dce6-b680-4a72-9277-4cfdab27cbbc
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IOleControl, IOleControl interface [COM], IOleControl interface [COM],described, _ctrl_iolecontrol, com.iolecontrol, ocidl/IOleControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IOleControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleControl interface


## -description


Provides the features for supporting keyboard mnemonics, ambient properties, and events in control objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleControl</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IOleControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08872f4f-eb3e-434c-bd7d-d4de621948ad">FreezeEvents</a>
</td>
<td align="left" width="63%">
Indicates whether the container is ignoring or accepting events from the control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/defb7509-e586-45a0-9e56-de9eba17f18e">GetControlInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the control's keyboard mnemonics and behavior.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ca43723-a14e-4f03-8eec-e10ab34ecb4d">OnAmbientPropertyChange</a>
</td>
<td align="left" width="63%">
Informs a control that one or more of the container's ambient properties has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b40afc9-89cf-4dfc-ab25-055bdf6964ce">OnMnemonic</a>
</td>
<td align="left" width="63%">
Informs a control that the user has pressed a keystroke that represents a keyboard mneumonic.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8b022f2c-d4b4-44ca-8e69-46e9aa20b3f9">IOleControlSite</a>



<a href="https://msdn.microsoft.com/ccddeae4-14fc-47df-a612-83d48a479b48">ISimpleFrameSite</a>
 

 

