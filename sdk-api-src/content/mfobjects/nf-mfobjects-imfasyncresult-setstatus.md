---
UID: NF:mfobjects.IMFAsyncResult.SetStatus
title: IMFAsyncResult::SetStatus (mfobjects.h)
description: Sets the status of the asynchronous operation. (IMFAsyncResult.SetStatus)
helpviewer_keywords: ["79dec067-ba54-435b-8744-9a6f43dd416d","IMFAsyncResult interface [Media Foundation]","SetStatus method","IMFAsyncResult.SetStatus","IMFAsyncResult::SetStatus","SetStatus","SetStatus method [Media Foundation]","SetStatus method [Media Foundation]","IMFAsyncResult interface","mf.imfasyncresult_setstatus","mfobjects/IMFAsyncResult::SetStatus"]
old-location: mf\imfasyncresult_setstatus.htm
tech.root: mf
ms.assetid: 79dec067-ba54-435b-8744-9a6f43dd416d
ms.date: 12/05/2018
ms.keywords: 79dec067-ba54-435b-8744-9a6f43dd416d, IMFAsyncResult interface [Media Foundation],SetStatus method, IMFAsyncResult.SetStatus, IMFAsyncResult::SetStatus, SetStatus, SetStatus method [Media Foundation], SetStatus method [Media Foundation],IMFAsyncResult interface, mf.imfasyncresult_setstatus, mfobjects/IMFAsyncResult::SetStatus
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
 - IMFAsyncResult::SetStatus
 - mfobjects/IMFAsyncResult::SetStatus
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
 - IMFAsyncResult.SetStatus
---

# IMFAsyncResult::SetStatus


## -description

Sets the status of the asynchronous operation.

## -parameters

### -param hrStatus [in]

The status of the asynchronous operation.

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

## -remarks

If you implement an asynchronous method, call <b>SetStatus</b> to set the status code for the operation.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a>
