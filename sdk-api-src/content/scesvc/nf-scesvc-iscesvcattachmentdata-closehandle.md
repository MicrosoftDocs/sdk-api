---
UID: NF:scesvc.ISceSvcAttachmentData.CloseHandle
title: ISceSvcAttachmentData::CloseHandle (scesvc.h)
description: The CloseHandle method closes a handle opened during a previous call to ISceSvcAttachmentData::Initialize.
helpviewer_keywords: ["CloseHandle","CloseHandle method [Security]","CloseHandle method [Security]","ISceSvcAttachmentData interface","ISceSvcAttachmentData interface [Security]","CloseHandle method","ISceSvcAttachmentData.CloseHandle","ISceSvcAttachmentData::CloseHandle","_config_iscesvcattachmentdata_closehandle","scesvc/ISceSvcAttachmentData::CloseHandle","security.iscesvcattachmentdata_closehandle"]
old-location: security\iscesvcattachmentdata_closehandle.htm
tech.root: security
ms.assetid: e50f5acf-06ef-49bb-bcf1-1fadeb4b808a
ms.date: 12/05/2018
ms.keywords: CloseHandle, CloseHandle method [Security], CloseHandle method [Security],ISceSvcAttachmentData interface, ISceSvcAttachmentData interface [Security],CloseHandle method, ISceSvcAttachmentData.CloseHandle, ISceSvcAttachmentData::CloseHandle, _config_iscesvcattachmentdata_closehandle, scesvc/ISceSvcAttachmentData::CloseHandle, security.iscesvcattachmentdata_closehandle
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISceSvcAttachmentData::CloseHandle
 - scesvc/ISceSvcAttachmentData::CloseHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsecedit.dll
api_name:
 - ISceSvcAttachmentData.CloseHandle
---

# ISceSvcAttachmentData::CloseHandle


## -description

The <b>CloseHandle</b> method closes a handle opened during a previous call to 
<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>.

## -parameters

### -param scesvcHandle [in]

The 
<a href="/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a> to close.

## -returns

The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates the method was successful.

## -remarks

You should call this method when your attachment snap-in extension no longer requires the handle returned by 
<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>.

## -see-also

<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a>



<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>