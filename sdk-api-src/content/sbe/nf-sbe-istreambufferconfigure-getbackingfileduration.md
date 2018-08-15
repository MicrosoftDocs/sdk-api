---
UID: NF:sbe.IStreamBufferConfigure.GetBackingFileDuration
title: IStreamBufferConfigure::GetBackingFileDuration
author: windows-sdk-content
description: The GetBackingFileDuration method retrieves the duration of each backing file.
old-location: mstv\istreambufferconfigure_getbackingfileduration.htm
old-project: mstv
ms.assetid: 3d02d87f-b617-4d46-82b2-41eb4b160d0f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetBackingFileDuration, GetBackingFileDuration method [Microsoft TV Technologies], GetBackingFileDuration method [Microsoft TV Technologies],IStreamBufferConfigure interface, IStreamBufferConfigure interface [Microsoft TV Technologies],GetBackingFileDuration method, IStreamBufferConfigure.GetBackingFileDuration, IStreamBufferConfigure::GetBackingFileDuration, IStreamBufferConfigureGetBackingFileDuration, mstv.istreambufferconfigure_getbackingfileduration, sbe/IStreamBufferConfigure::GetBackingFileDuration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferConfigure.GetBackingFileDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IStreamBufferConfigure::GetBackingFileDuration


## -description


The <b>GetBackingFileDuration</b> method retrieves the duration of each backing file.


## -parameters




### -param pdwSeconds [out]

Pointer to a variable that receives the file duration, in seconds.


## -returns



Returns an <b>HRESULT</b>. Possible values include those in the following table.

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
 




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure Interface</a>
 

 

