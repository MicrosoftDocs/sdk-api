---
UID: NF:sbe.IStreamBufferConfigure.GetBackingFileCount
title: IStreamBufferConfigure::GetBackingFileCount
author: windows-driver-content
description: The GetBackingFileCount method retrieves the maximum and minimum number of backing files.
old-location: mstv\istreambufferconfigure_getbackingfilecount.htm
old-project: mstv
ms.assetid: 5bf2a99a-ed6b-4ce6-9190-756393afcef0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetBackingFileCount, GetBackingFileCount method [Microsoft TV Technologies], GetBackingFileCount method [Microsoft TV Technologies],IStreamBufferConfigure interface, IStreamBufferConfigure interface [Microsoft TV Technologies],GetBackingFileCount method, IStreamBufferConfigure.GetBackingFileCount, IStreamBufferConfigure::GetBackingFileCount, IStreamBufferConfigureGetBackingFileCount, mstv.istreambufferconfigure_getbackingfilecount, sbe/IStreamBufferConfigure::GetBackingFileCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferConfigure.GetBackingFileCount
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStreamBufferConfigure::GetBackingFileCount


## -description


The <b>GetBackingFileCount</b> method retrieves the maximum and minimum number of backing files.


## -parameters




### -param pdwMin [out]

Pointer to a variable that receives the backing file minimum.


### -param pdwMax [out]

Pointer to a variable that receives the backing file maximum.


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
 




## -remarks



If the reader lags behind the writer by more than <i>pdwMin</i> files, the writer starts to send STREAMBUFFER_EC_CONTENT_BECOMING_STALE events. If the reader lags behind the writer by more than <i>pdwMax</i> files, the writer begins to overwrite files and sends an STREAMBUFFER_EC_STALE_FILE_DELETED event.




## -see-also




<a href="https://msdn.microsoft.com/8874fefd-2241-4b04-a7d5-191e13743fa0">IStreamBufferConfigure Interface</a>
 

 

