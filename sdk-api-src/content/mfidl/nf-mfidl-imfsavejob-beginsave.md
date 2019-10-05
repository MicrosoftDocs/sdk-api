---
UID: NF:mfidl.IMFSaveJob.BeginSave
title: IMFSaveJob::BeginSave (mfidl.h)
author: windows-sdk-content
description: Begins saving a Windows Media file to the application's byte stream.
old-location: mf\imfsavejob_beginsave.htm
tech.root: medfound
ms.assetid: ff137b76-2a05-4e58-8d4f-d12cdd89656b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BeginSave, BeginSave method [Media Foundation], BeginSave method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],BeginSave method, IMFSaveJob.BeginSave, IMFSaveJob::BeginSave, ff137b76-2a05-4e58-8d4f-d12cdd89656b, mf.imfsavejob_beginsave, mfidl/IMFSaveJob::BeginSave
ms.topic: method
f1_keywords: 
 - "mfidl/IMFSaveJob.BeginSave"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSaveJob.BeginSave
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSaveJob::BeginSave


## -description



Begins saving a Windows Media file to the application's byte stream.




## -parameters




### -param pStream [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface of the application's byte stream. The data from the source byte stream is written to this byte stream.


### -param pCallback [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface


### -param pState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.


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



When the operation completes, the callback object's <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-endsave">IMFSaveJob::EndSave</a> to complete the asynchronous request.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsavejob">IMFSaveJob</a>
 

 

