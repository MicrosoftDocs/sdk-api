---
UID: NF:bdatif.IMPEG2_TIF_CONTROL.UnregisterTIF
title: IMPEG2_TIF_CONTROL::UnregisterTIF
author: windows-sdk-content
description: The UnregisterTIF method unregisters the TIF with the Network Provider.
old-location: mstv\impeg2_tif_control_unregistertif.htm
old-project: mstv
ms.assetid: e4fd151e-ec24-41b9-85df-fba05fc174d1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMPEG2_TIF_CONTROL interface [Microsoft TV Technologies],UnregisterTIF method, IMPEG2_TIF_CONTROL.UnregisterTIF, IMPEG2_TIF_CONTROL::UnregisterTIF, IMPEG2_TIF_CONTROLUnregisterTIF, UnregisterTIF, UnregisterTIF method [Microsoft TV Technologies], UnregisterTIF method [Microsoft TV Technologies],IMPEG2_TIF_CONTROL interface, bdatif/IMPEG2_TIF_CONTROL::UnregisterTIF, mstv.impeg2_tif_control_unregistertif
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
 - IMPEG2_TIF_CONTROL.UnregisterTIF
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMPEG2_TIF_CONTROL::UnregisterTIF


## -description



The <b>UnregisterTIF</b> method unregisters the TIF with the Network Provider.




## -parameters




### -param pvRegistrationContext [in]

Identifier returned by the <a href="https://msdn.microsoft.com/d17b1f6b-24f4-40f4-9a58-aa582c0958f8">IMPEG2_TIF_CONTROL::RegisterTIF</a> method.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -remarks



Call this method after the TIF's intput pin has been disconnected from the Demux.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL Interface</a>
 

 

