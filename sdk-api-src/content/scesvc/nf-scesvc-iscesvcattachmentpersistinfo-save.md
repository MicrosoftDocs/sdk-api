---
UID: NF:scesvc.ISceSvcAttachmentPersistInfo.Save
title: ISceSvcAttachmentPersistInfo::Save (scesvc.h)
description: The Save method causes the snap-in extension to return information about the data that needs to be saved. The caller is responsible for saving the data.
helpviewer_keywords: ["ISceSvcAttachmentPersistInfo interface [Security]","Save method","ISceSvcAttachmentPersistInfo.Save","ISceSvcAttachmentPersistInfo::Save","Save","Save method [Security]","Save method [Security]","ISceSvcAttachmentPersistInfo interface","_config_iscesvcattachmentpersistinfo_save","scesvc/ISceSvcAttachmentPersistInfo::Save","security.iscesvcattachmentpersistinfo_save"]
old-location: security\iscesvcattachmentpersistinfo_save.htm
tech.root: security
ms.assetid: bdec64b8-2a92-4165-95ff-0de981f2d878
ms.date: 12/05/2018
ms.keywords: ISceSvcAttachmentPersistInfo interface [Security],Save method, ISceSvcAttachmentPersistInfo.Save, ISceSvcAttachmentPersistInfo::Save, Save, Save method [Security], Save method [Security],ISceSvcAttachmentPersistInfo interface, _config_iscesvcattachmentpersistinfo_save, scesvc/ISceSvcAttachmentPersistInfo::Save, security.iscesvcattachmentpersistinfo_save
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
 - ISceSvcAttachmentPersistInfo::Save
 - scesvc/ISceSvcAttachmentPersistInfo::Save
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
 - ISceSvcAttachmentPersistInfo.Save
---

# ISceSvcAttachmentPersistInfo::Save


## -description

The <b>Save</b> method causes the snap-in extension to return information about the data that needs to be saved. The caller is responsible for saving the data.

## -parameters

### -param lpTemplateName [in]

Pointer to a null-terminated string that contains the security template name to save data to.

### -param scesvcHandle [in]

Pointer that receives the 
<a href="/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a> the attachment snap-in extension is using to communicate with the Security Configuration snap-ins.

### -param ppvData [out]

Pointer that receives a buffer that contains the data to be saved.

### -param pbOverwriteAll [out]

Pointer to a <b>BOOL</b> that receives a value indicating whether preexisting data should be overwritten.

## -returns

The return value is an HRESULT. A value of S_OK indicates the method was successful.

## -remarks

The caller should free the buffer set in <i>ppvData</i> by calling 
<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer">ISceSvcAttachmentPersistInfo::FreeBuffer</a>.

## -see-also

<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a>



<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer">ISceSvcAttachmentPersistInfo::FreeBuffer</a>



<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-isdirty">ISceSvcAttachmentPersistInfo::IsDirty</a>



<a href="/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a>