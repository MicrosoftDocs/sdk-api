---
UID: NF:mfidl.IMFSaveJob.EndSave
title: IMFSaveJob::EndSave (mfidl.h)
description: Completes the operation started by IMFSaveJob::BeginSave.
helpviewer_keywords: ["9d63d7b5-4454-4301-b467-eea82bace6ff","EndSave","EndSave method [Media Foundation]","EndSave method [Media Foundation]","IMFSaveJob interface","IMFSaveJob interface [Media Foundation]","EndSave method","IMFSaveJob.EndSave","IMFSaveJob::EndSave","mf.imfsavejob_endsave","mfidl/IMFSaveJob::EndSave"]
old-location: mf\imfsavejob_endsave.htm
tech.root: mf
ms.assetid: 9d63d7b5-4454-4301-b467-eea82bace6ff
ms.date: 12/05/2018
ms.keywords: 9d63d7b5-4454-4301-b467-eea82bace6ff, EndSave, EndSave method [Media Foundation], EndSave method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],EndSave method, IMFSaveJob.EndSave, IMFSaveJob::EndSave, mf.imfsavejob_endsave, mfidl/IMFSaveJob::EndSave
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSaveJob::EndSave
 - mfidl/IMFSaveJob::EndSave
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
 - IMFSaveJob.EndSave
---

# IMFSaveJob::EndSave


## -description

Completes the operation started by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-beginsave">IMFSaveJob::BeginSave</a>.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

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

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob">IMFSaveJob</a>