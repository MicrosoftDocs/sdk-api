---
UID: NF:fsrmquota.IFsrmQuotaTemplate.CopyTemplate
title: IFsrmQuotaTemplate::CopyTemplate (fsrmquota.h)
description: Copies the property values of the specified template to this template. (IFsrmQuotaTemplate.CopyTemplate)
helpviewer_keywords: ["CopyTemplate","CopyTemplate method [File Server Resource Manager]","CopyTemplate method [File Server Resource Manager]","IFsrmQuotaTemplate interface","IFsrmQuotaTemplate interface [File Server Resource Manager]","CopyTemplate method","IFsrmQuotaTemplate.CopyTemplate","IFsrmQuotaTemplate::CopyTemplate","fs.ifsrmquotatemplate_copytemplate","fsrm.ifsrmquotatemplate_copytemplate","fsrmquota/IFsrmQuotaTemplate::CopyTemplate"]
old-location: fsrm\ifsrmquotatemplate_copytemplate.htm
tech.root: fsrm
ms.assetid: 00aa7693-3c6e-4688-915e-59c31e5b8e6e
ms.date: 12/05/2018
ms.keywords: CopyTemplate, CopyTemplate method [File Server Resource Manager], CopyTemplate method [File Server Resource Manager],IFsrmQuotaTemplate interface, IFsrmQuotaTemplate interface [File Server Resource Manager],CopyTemplate method, IFsrmQuotaTemplate.CopyTemplate, IFsrmQuotaTemplate::CopyTemplate, fs.ifsrmquotatemplate_copytemplate, fsrm.ifsrmquotatemplate_copytemplate, fsrmquota/IFsrmQuotaTemplate::CopyTemplate
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
 - IFsrmQuotaTemplate::CopyTemplate
 - fsrmquota/IFsrmQuotaTemplate::CopyTemplate
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
 - IFsrmQuotaTemplate.CopyTemplate
---

# IFsrmQuotaTemplate::CopyTemplate


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Copies the property values of the specified template to this template.

## -parameters

### -param quotaTemplateName [in]

The name of the template from which to copy the property values. The string is limited to 4,000 
      characters.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplate">IFsrmQuotaTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
