---
UID: NF:mfobjects.IMFAsyncResult.GetStatus
title: IMFAsyncResult::GetStatus (mfobjects.h)
description: Returns the status of the asynchronous operation. (IMFAsyncResult.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method [Media Foundation]","GetStatus method [Media Foundation]","IMFAsyncResult interface","IMFAsyncResult interface [Media Foundation]","GetStatus method","IMFAsyncResult.GetStatus","IMFAsyncResult::GetStatus","ad99f3dd-4885-42e8-8f4e-060d522dde7b","mf.imfasyncresult_getstatus","mfobjects/IMFAsyncResult::GetStatus"]
old-location: mf\imfasyncresult_getstatus.htm
tech.root: mf
ms.assetid: ad99f3dd-4885-42e8-8f4e-060d522dde7b
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Media Foundation], GetStatus method [Media Foundation],IMFAsyncResult interface, IMFAsyncResult interface [Media Foundation],GetStatus method, IMFAsyncResult.GetStatus, IMFAsyncResult::GetStatus, ad99f3dd-4885-42e8-8f4e-060d522dde7b, mf.imfasyncresult_getstatus, mfobjects/IMFAsyncResult::GetStatus
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAsyncResult::GetStatus
 - mfobjects/IMFAsyncResult::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAsyncResult.GetStatus
---

# IMFAsyncResult::GetStatus


## -description

Returns the status of the asynchronous operation.



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
The operation completed successfully.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a>
