---
UID: NF:mfidl.IMFSaveJob.CancelSave
title: IMFSaveJob::CancelSave (mfidl.h)
description: Cancels the operation started by IMFSaveJob::BeginSave.
helpviewer_keywords: ["CancelSave","CancelSave method [Media Foundation]","CancelSave method [Media Foundation]","IMFSaveJob interface","IMFSaveJob interface [Media Foundation]","CancelSave method","IMFSaveJob.CancelSave","IMFSaveJob::CancelSave","ce3ec53a-eeca-430f-a939-3d941b9b2570","mf.imfsavejob_cancelsave","mfidl/IMFSaveJob::CancelSave"]
old-location: mf\imfsavejob_cancelsave.htm
tech.root: mf
ms.assetid: ce3ec53a-eeca-430f-a939-3d941b9b2570
ms.date: 12/05/2018
ms.keywords: CancelSave, CancelSave method [Media Foundation], CancelSave method [Media Foundation],IMFSaveJob interface, IMFSaveJob interface [Media Foundation],CancelSave method, IMFSaveJob.CancelSave, IMFSaveJob::CancelSave, ce3ec53a-eeca-430f-a939-3d941b9b2570, mf.imfsavejob_cancelsave, mfidl/IMFSaveJob::CancelSave
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
 - IMFSaveJob::CancelSave
 - mfidl/IMFSaveJob::CancelSave
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
 - IMFSaveJob.CancelSave
---

# IMFSaveJob::CancelSave


## -description

Cancels the operation started by <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsavejob-beginsave">IMFSaveJob::BeginSave</a>.



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
