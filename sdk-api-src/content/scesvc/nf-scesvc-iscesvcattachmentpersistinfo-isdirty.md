---
UID: NF:scesvc.ISceSvcAttachmentPersistInfo.IsDirty
title: ISceSvcAttachmentPersistInfo::IsDirty (scesvc.h)
description: The IsDirty method returns a value indicating whether data in the attachment snap-in has been modified since it was last saved.
helpviewer_keywords: ["ISceSvcAttachmentPersistInfo interface [Security]","IsDirty method","ISceSvcAttachmentPersistInfo.IsDirty","ISceSvcAttachmentPersistInfo::IsDirty","IsDirty","IsDirty method [Security]","IsDirty method [Security]","ISceSvcAttachmentPersistInfo interface","_config_iscesvcattachmentpersistinfo_isdirty","scesvc/ISceSvcAttachmentPersistInfo::IsDirty","security.iscesvcattachmentpersistinfo_isdirty"]
old-location: security\iscesvcattachmentpersistinfo_isdirty.htm
tech.root: security
ms.assetid: b430e598-e16c-47fc-8f19-fbcfc6b71337
ms.date: 12/05/2018
ms.keywords: ISceSvcAttachmentPersistInfo interface [Security],IsDirty method, ISceSvcAttachmentPersistInfo.IsDirty, ISceSvcAttachmentPersistInfo::IsDirty, IsDirty, IsDirty method [Security], IsDirty method [Security],ISceSvcAttachmentPersistInfo interface, _config_iscesvcattachmentpersistinfo_isdirty, scesvc/ISceSvcAttachmentPersistInfo::IsDirty, security.iscesvcattachmentpersistinfo_isdirty
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
 - ISceSvcAttachmentPersistInfo::IsDirty
 - scesvc/ISceSvcAttachmentPersistInfo::IsDirty
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
 - ISceSvcAttachmentPersistInfo.IsDirty
---

# ISceSvcAttachmentPersistInfo::IsDirty


## -description

The <b>IsDirty</b> method returns a value indicating whether data in the attachment snap-in has been modified since it was last saved.

## -parameters

### -param lpTemplateName [in]

Pointer to a null-terminated string that contains a security template name. Multiple security templates can be modified so that each service extension can be expanded under multiple templates.

## -returns

The return value is an HRESULT. A value of S_OK indicates the method was successful.

## -see-also

<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a>



<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-save">ISceSvcAttachmentPersistInfo::Save</a>