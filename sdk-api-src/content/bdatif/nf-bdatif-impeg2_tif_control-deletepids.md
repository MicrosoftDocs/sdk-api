---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.DeletePIDs
title: IMPEG2_TIF_CONTROL::DeletePIDs
author: windows-sdk-content
description: The DeletePIDs method informs the Network Provider that the TIF no longer requires the specified PID.
old-location: mstv\impeg2_tif_control_deletepids.htm
old-project: mstv
ms.assetid: d5188e30-6980-482f-a690-494855d6aeea
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: DeletePIDs, DeletePIDs method [Microsoft TV Technologies], DeletePIDs method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],DeletePIDs method, IMPEG2_TIF_CONTROL.DeletePIDs, IMPEG2_TIF_CONTROL::DeletePIDs, IMPEG2_TIF_CONTROLDeletePIDs, bdatif/IMPEG2_TIF_CONTROL::DeletePIDs, mstv.impeg2_tif_control_deletepids
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
 - IMPEG2_TIF_CONTROL.DeletePIDs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMPEG2_TIF_CONTROL::DeletePIDs


## -description



The <b>DeletePIDs</b> method informs the Network Provider that the TIF no longer requires the specified PID.




## -parameters




### -param ulcPIDs [in]

Specifies the number of PIDs to delete. This value must equal the number of elements in the array specified by <i>pulPIDs</i>.


### -param pulPIDs [in]

Specifies an array of PID values containing <i>ulcPIDs</i> elements.


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



This method is called if a set of tables in the transport stream goes away, in order to remove the PSI/SI MPEG2 packet IDs from the TIF's data stream.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL Interface</a>
 

 

