---
UID: NF:tapi3if.ITCallHub.Clear
title: ITCallHub::Clear
author: windows-sdk-content
description: The Clear method attempts to remove all calls and participants from CallHub. The application may not have the privileges required to disconnect every call.
old-location: tapi3\itcallhub_clear.htm
tech.root: Tapi
ms.assetid: 87799da3-73c3-469a-badf-884dcfe774e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clear, Clear method [TAPI 2.2], Clear method [TAPI 2.2],ITCallHub interface, ITCallHub interface [TAPI 2.2],Clear method, ITCallHub.Clear, ITCallHub::Clear, _tapi3_itcallhub_clear, tapi3.itcallhub_clear, tapi3if/ITCallHub::Clear
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITCallHub.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallHub::Clear


## -description


The 
<b>Clear</b> method attempts to remove all calls and participants from CallHub. The application may not have the privileges required to disconnect every call.


## -parameters






## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>
 

 

