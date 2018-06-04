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

# _DDTRANSFERININFO structure


## -description


The DDTRANSFERININFO structure contains the transfer information for the surface 


## -struct-fields




### -field lpSurfaceData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a> structure that represents the surface that contains the information to be transferred. The information in this structure is supplied by DirectDraw. 


### -field dwStartLine

Indicates the first line in the surface from which data is transferred. 


### -field dwEndLine

Indicates the last line in the surface from which data is transferred, inclusive. 


### -field dwTransferID

Specifies an identification for the transfer supplied by DirectDraw. This transfer ID is used by the driver in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549521">DDGETTRANSFERSTATUSOUTINFO</a> structure. 


### -field dwTransferFlags

Indicates the type of transfer. One of the following: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDTRANSFER_CANCEL

</td>
<td>
DirectDraw previously requested a transfer, but is now canceling that request.

</td>
</tr>
<tr>
<td>
DDTRANSFER_HALFLINES

</td>
<td>
Due to half line issues, the odd field contains an extra line of useless data at the top that the driver must account for.

</td>
</tr>
<tr>
<td>
DDTRANSFER_INVERT

</td>
<td>
During bus mastering, the capture driver is requesting an inversion.

</td>
</tr>
<tr>
<td>
DDTRANSFER_NONLOCALVIDMEM

</td>
<td>
The transfer is from display memory to AGP memory.

</td>
</tr>
<tr>
<td>
DDTRANSFER_SYSTEMMEMORY

</td>
<td>
The transfer is from display memory to system memory.

</td>
</tr>
</table>
 


### -field lpDestMDL

Points to a destination <a href="https://msdn.microsoft.com/a1ec4764-4e11-4fb2-b439-ad6b721eb504">memory descriptor list (MDL)</a> structure. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff549521">DDGETTRANSFERSTATUSOUTINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550335">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

