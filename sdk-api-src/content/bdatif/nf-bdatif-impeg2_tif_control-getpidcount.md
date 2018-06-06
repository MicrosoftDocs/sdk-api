---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.GetPIDCount
title: IMPEG2_TIF_CONTROL::GetPIDCount
author: windows-sdk-content
description: The GetPIDCount method retrieves the number of MPEG-2 Packet IDs being filtered by the MPEG-2 Demultiplexer into the TIF's input data.
old-location: mstv\impeg2_tif_control_getpidcount.htm
old-project: mstv
ms.assetid: 2d77c3d8-b91c-43de-b4c1-bd41636eb4ad
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetPIDCount, GetPIDCount method [Microsoft TV Technologies], GetPIDCount method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],GetPIDCount method, IMPEG2_TIF_CONTROL.GetPIDCount, IMPEG2_TIF_CONTROL::GetPIDCount, IMPEG2_TIF_CONTROLGetPIDCount, bdatif/IMPEG2_TIF_CONTROL::GetPIDCount, mstv.impeg2_tif_control_getpidcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdatif.h
req.include-header: 
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
tech.root: 
req.typenames: SmartCardApplication
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IMPEG2_TIF_CONTROL.GetPIDCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMPEG2_TIF_CONTROL::GetPIDCount


## -description



The <b>GetPIDCount</b> method retrieves the number of MPEG-2 Packet IDs being filtered by the <a href="https://msdn.microsoft.com/99bfc55d-6519-4e85-98ce-cad27bd71ffb">MPEG-2 Demultiplexer</a> into the TIF's input data.




## -parameters




### -param pulcPIDs [out]

Pointer to a variable that receives the number of PIDs currently being filtered to the Demux.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



A custom TIF extension might or might not need this method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL Interface</a>



<a href="https://msdn.microsoft.com/c7ca141b-e471-47ce-96b5-b2c0cad89daf">IMPEG2_TIF_CONTROL::GetPIDs</a>
 

 

