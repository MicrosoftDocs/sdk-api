---
UID: NS:dxmini._DDTRANSFERININFO
title: "_DDTRANSFERININFO"
author: windows-sdk-content
description: The DDTRANSFERININFO structure contains the transfer information for the surface
old-location: display\ddtransferininfo.htm
tech.root: display
ms.assetid: 9e5f938d-0db6-4df6-a9c2-49840fef8c03
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PDDTRANSFERININFO, DDTRANSFERININFO, DDTRANSFERININFO structure [Display Devices], PDDTRANSFERININFO, PDDTRANSFERININFO structure pointer [Display Devices], Video_Structs_2585fa9a-a3ea-4bc0-a5b8-1911262203ba.xml, _DDTRANSFERININFO, display.ddtransferininfo, dxmini/DDTRANSFERININFO, dxmini/PDDTRANSFERININFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDTRANSFERININFO
product: Windows
targetos: Windows
req.typenames: DDTRANSFERININFO, *PDDTRANSFERININFO
req.redist: 
---

# _DDTRANSFERININFO structure


## -description


The DDTRANSFERININFO structure contains the transfer information for the surface 


## -struct-fields




### -field lpSurfaceData

Points to a <a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a> structure that represents the surface that contains the information to be transferred. The information in this structure is supplied by DirectDraw. 


### -field dwStartLine

Indicates the first line in the surface from which data is transferred. 


### -field dwEndLine

Indicates the last line in the surface from which data is transferred, inclusive. 


### -field dwTransferID

Specifies an identification for the transfer supplied by DirectDraw. This transfer ID is used by the driver in the <a href="https://msdn.microsoft.com/593a42be-e1e9-41e5-a006-1513c5aa5226">DDGETTRANSFERSTATUSOUTINFO</a> structure. 


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




<a href="https://msdn.microsoft.com/593a42be-e1e9-41e5-a006-1513c5aa5226">DDGETTRANSFERSTATUSOUTINFO</a>



<a href="https://msdn.microsoft.com/4057cfcf-675e-439f-8b51-23adede1d35a">DDSURFACEDATA</a>



<a href="https://msdn.microsoft.com/62e1a5f6-9777-4acf-a531-b3554eaf89a6">DxTransfer</a>
 

 

