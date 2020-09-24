---
UID: NF:scesvc.ISceSvcAttachmentData.Initialize
title: ISceSvcAttachmentData::Initialize (scesvc.h)
description: The Initialize method informs the Security Configuration snap-in that the snap-in extension is loaded, and it establishes a context for communications.
helpviewer_keywords: ["ISceSvcAttachmentData interface [Security]","Initialize method","ISceSvcAttachmentData.Initialize","ISceSvcAttachmentData::Initialize","Initialize","Initialize method [Security]","Initialize method [Security]","ISceSvcAttachmentData interface","_config_iscesvcattachmentdata_initialize","scesvc/ISceSvcAttachmentData::Initialize","security.iscesvcattachmentdata_initialize"]
old-location: security\iscesvcattachmentdata_initialize.htm
tech.root: security
ms.assetid: 2c5d087d-774b-4cfb-a458-9a5b1c6106c7
ms.date: 12/05/2018
ms.keywords: ISceSvcAttachmentData interface [Security],Initialize method, ISceSvcAttachmentData.Initialize, ISceSvcAttachmentData::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISceSvcAttachmentData interface, _config_iscesvcattachmentdata_initialize, scesvc/ISceSvcAttachmentData::Initialize, security.iscesvcattachmentdata_initialize
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
 - ISceSvcAttachmentData::Initialize
 - scesvc/ISceSvcAttachmentData::Initialize
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
 - ISceSvcAttachmentData.Initialize
---

# ISceSvcAttachmentData::Initialize


## -description

The <b>Initialize</b> method informs the Security Configuration snap-in that the snap-in extension is loaded, and it establishes a context for communications.

## -parameters

### -param lpServiceName [in]

String that specifies the name of the security service to retrieve information about.

### -param lpTemplateName [in]

String that specifies the name of the template.

### -param lpSceSvcPersistInfo [in]

Pointer to the 
<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a> interface of the attachment snap-in extension.

### -param pscesvcHandle [out]

Pointer that receives an 
<a href="/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a> that represents the communication context between the Security Configuration snap-in and the snap-in extension. This handle is passed in as a parameter to the other <a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a> methods. When the attachment snap-in extension no longer needs this handle, free it by calling 
<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-closehandle">ISceSvcAttachmentData::CloseHandle</a>.

## -returns

The return value is an HRESULT. A value of S_OK indicates the method was successful.

## -see-also

<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a>



<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-closehandle">ISceSvcAttachmentData::CloseHandle</a>



<a href="/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a>



<a href="/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a>