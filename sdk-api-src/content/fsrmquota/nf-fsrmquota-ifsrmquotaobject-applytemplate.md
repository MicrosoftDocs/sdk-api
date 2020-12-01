---
UID: NF:fsrmquota.IFsrmQuotaObject.ApplyTemplate
title: IFsrmQuotaObject::ApplyTemplate (fsrmquota.h)
description: Applies the property values of the specified quota template to this quota object.
helpviewer_keywords: ["ApplyTemplate","ApplyTemplate method [File Server Resource Manager]","ApplyTemplate method [File Server Resource Manager]","IFsrmQuotaObject interface","IFsrmQuotaObject interface [File Server Resource Manager]","ApplyTemplate method","IFsrmQuotaObject.ApplyTemplate","IFsrmQuotaObject::ApplyTemplate","fs.ifsrmquotaobject_applytemplate","fsrm.ifsrmquotaobject_applytemplate","fsrmquota/IFsrmQuotaObject::ApplyTemplate"]
old-location: fsrm\ifsrmquotaobject_applytemplate.htm
tech.root: fsrm
ms.assetid: f4e65d53-7841-4f84-9c14-bad43089a87f
ms.date: 12/05/2018
ms.keywords: ApplyTemplate, ApplyTemplate method [File Server Resource Manager], ApplyTemplate method [File Server Resource Manager],IFsrmQuotaObject interface, IFsrmQuotaObject interface [File Server Resource Manager],ApplyTemplate method, IFsrmQuotaObject.ApplyTemplate, IFsrmQuotaObject::ApplyTemplate, fs.ifsrmquotaobject_applytemplate, fsrm.ifsrmquotaobject_applytemplate, fsrmquota/IFsrmQuotaObject::ApplyTemplate
req.header: fsrmquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: SrmSvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmQuotaObject::ApplyTemplate
 - fsrmquota/IFsrmQuotaObject::ApplyTemplate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaObject.ApplyTemplate
---

# IFsrmQuotaObject::ApplyTemplate


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Applies the property values of the specified quota template to this quota object.

## -parameters

### -param quotaTemplateName [in]

The name of the quota template.  The string is limited to 4,000 characters.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>