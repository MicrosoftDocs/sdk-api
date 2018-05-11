---
UID: NF:sbe.IStreamBufferConfigure3.GetNamespace
title: IStreamBufferConfigure3::GetNamespace
author: windows-driver-content
description: The GetNamespace method retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.
old-location: mstv\istreambufferconfigure3_getnamespace.htm
old-project: mstv
ms.assetid: c03b5edd-e2b2-4ac9-b2e7-080f3796a6cc
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetNamespace, GetNamespace method [Microsoft TV Technologies], GetNamespace method [Microsoft TV Technologies],IStreamBufferConfigure3 interface, IStreamBufferConfigure3 interface [Microsoft TV Technologies],GetNamespace method, IStreamBufferConfigure3.GetNamespace, IStreamBufferConfigure3::GetNamespace, IStreamBufferConfigure3GetNamespace, mstv.istreambufferconfigure3_getnamespace, sbe/IStreamBufferConfigure3::GetNamespace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	IStreamBufferConfigure3.GetNamespace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStreamBufferConfigure3::GetNamespace


## -description


The <b>GetNamespace</b> method retrieves the prefix that is added to the names of the synchronization objects that the Stream Buffer Engine uses to synchronize the reader and writer.


## -parameters




### -param ppszNamespace [out]

Receives a pointer to a null-terminated, wide-character string. The caller must free the string by calling <b>CoTaskMemFree</b>. If no prefix is defined, this variable receives a <b>NULL</b> pointer.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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




<a href="https://msdn.microsoft.com/73f3cd43-11d1-4eff-861d-087bfda7d135">IStreamBufferConfigure3 Interface</a>
 

 

