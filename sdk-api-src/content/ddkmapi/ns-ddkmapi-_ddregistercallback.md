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

# _DDREGISTERCALLBACK structure


## -description


The DDREGISTERCALLBACK structure contains the register callback information. This structure is used by both the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551502">DD_DXAPI_REGISTER_CALLBACK</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/ff551514">DD_DXAPI_UNREGISTER_CALLBACK</a> function identifiers of the <b>DxApi</b> function. 


## -struct-fields




### -field hDirectDraw

Specifies the Microsoft DirectDraw handle.


### -field dwEvents

Defines the event that should trigger the callback. The values in <b>dwParam1</b> and <b>dwParam2</b> depend on the event. The following events are defined:

<table>
<tr>
<th>Event</th>
<th>Description</th>
<th>dwParam1,dwParam2</th>
</tr>
<tr>
<td>
DDEVENT_DISPLAY_VSYNC

</td>
<td>
Called every time a display V-sync occurs.

</td>
<td>

<dl>
<dt>unused,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_POSTDOSBOX

</td>
<td>
Called after returning from a full-screen MS-DOS box or the security dialog box (appears when CTRL+ALT+DELETE is pressed).

</td>
<td>

<dl>
<dt>unused,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_POSTRESCHANGE

</td>
<td>
Called after a mode change occurs.

</td>
<td>

<dl>
<dt>unused,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_PREDOSBOX

</td>
<td>
Called before entering a full-screen MS-DOS box or the security dialog box (appears when CTRL+ALT+DELETE is pressed).

</td>
<td>

<dl>
<dt>unused,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_PRERESCHANGE

</td>
<td>
Called before a mode change occurs.

</td>
<td>

<dl>
<dt>unused,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_VP_LINE

</td>
<td>
Sets an IRQ to occur each time the hardware video port writes the specified line and then calls the callback each time the IRQ is triggered.

</td>
<td>

<dl>
<dt>hVideoPort,</dt>
<dt>line</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDEVENT_VP_VSYNC

</td>
<td>
Called each time a hardware video port V-sync occurs.

</td>
<td>

<dl>
<dt>hVideoPort,</dt>
<dt>unused</dt>
</dl>


</td>
</tr>
</table>
 


### -field pfnCallback

Points to a <a href="https://msdn.microsoft.com/ee581d7b-c3b8-47e5-bae8-348b22ea0f95">pfnCallback</a> callback function that is called when the event that is specified by the <b>dwEvents</b> member occurs.


### -field dwParam1

Defined by the <b>dwEvents</b> member.


### -field dwParam2

Defined by the <b>dwEvents</b> member.


### -field pContext

Contains client data that is passed back to the client if the <b>pfnCallback</b> callback function is called.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551502">DD_DXAPI_REGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551514">DD_DXAPI_UNREGISTER_CALLBACK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557364">DxApi</a>
 

 

