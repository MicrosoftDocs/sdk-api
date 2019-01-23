---
UID: NN:dwrite_3.IDWriteAsyncResult
title: IDWriteAsyncResult
author: windows-sdk-content
description: Represents the result of an asynchronous operation. A client can use the interface to wait for the operation to complete and to get the result.
old-location: directwrite\idwriteasyncresult.htm
tech.root: DirectWrite
ms.assetid: 8F267213-EB98-4AD9-826A-7D4E34FEB3E4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteAsyncResult, IDWriteAsyncResult interface [Direct Write], IDWriteAsyncResult interface [Direct Write],described, directwrite.idwriteasyncresult, dwrite_3/IDWriteAsyncResult
ms.topic: interface
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteAsyncResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteAsyncResult interface


## -description


Represents the result of an asynchronous
          operation. A client can use the interface to wait for the operation to
          complete and to get the result.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteAsyncResult</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteAsyncResult</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteAsyncResult</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40588741-958D-4D7E-8E39-206D7CFCBFB6">GetResult</a>
</td>
<td align="left" width="63%">
Returns the result of the asynchronous operation. The return value is E_PENDING if the operation has not yet completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BF7F7A94-AD3E-48DB-9A01-D4E615063A8F">GetWaitHandle</a>
</td>
<td align="left" width="63%">
Returns a handle that can be used to wait for the asynchronous operation to complete. The handle remains valid until the interface is released.

</td>
</tr>
</table> 


## -remarks



IDWriteAsyncResult is returned by <a href="https://msdn.microsoft.com/A0EE8383-81A8-4974-B213-142704EFA210">IDWriteRemoteFontFileStream::BeginDownload</a> for signaling completion of a font download operation.



