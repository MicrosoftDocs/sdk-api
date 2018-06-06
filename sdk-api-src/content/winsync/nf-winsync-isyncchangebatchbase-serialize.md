---
UID: NF:winsync.ISyncChangeBatchBase.Serialize
title: ISyncChangeBatchBase::Serialize
author: windows-sdk-content
description: Serializes the change batch to an array of bytes.
old-location: winsync\isyncchangebatchbase_serialize.htm
old-project: winsync
ms.assetid: 785a763c-99a2-45d1-b42b-9673aedc5c5d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ISyncChangeBatchBase interface [Windows Sync],Serialize method, ISyncChangeBatchBase.Serialize, ISyncChangeBatchBase::Serialize, Serialize, Serialize method [Windows Sync], Serialize method [Windows Sync],ISyncChangeBatchBase interface, winsync.isyncchangebatchbase_serialize, winsync/ISyncChangeBatchBase::Serialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchBase.Serialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase::Serialize


## -description


Serializes the change batch to an array of bytes.


## -parameters




### -param pbChangeBatch [in, out]

The byte array that receives the change batch data.


### -param pcbChangeBatch [in, out]

Specifies the number of bytes in <i>pbChangeBatch</i>. Returns the number of bytes required for <i>pbChangeBatch</i> when <i>pbChangeBatch</i> is too small, or the number of bytes written to <i>pbChangeBatch</i> when data is written.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
<i>pbChangeBatch</i> is too small. In this case, the required number of bytes is stored in <i>pcbChangeBatch</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The last group added to the batch was not ended.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/840a1f5e-56f7-4774-a154-0dab66c3d407">SyncSerializationVersion Enumeration</a>
 

 

