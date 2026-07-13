---
UID: NF:fsrmquota.IFsrmQuotaTemplate.put_Name
title: IFsrmQuotaTemplate::put_Name (fsrmquota.h)
description: Retrieves and sets the name of the quota template. (Put)
helpviewer_keywords: ["IFsrmQuotaTemplate interface [File Server Resource Manager]","Name property","IFsrmQuotaTemplate.Name","IFsrmQuotaTemplate.put_Name","IFsrmQuotaTemplate::Name","IFsrmQuotaTemplate::get_Name","IFsrmQuotaTemplate::put_Name","Name property [File Server Resource Manager]","Name property [File Server Resource Manager]","IFsrmQuotaTemplate interface","fs.ifsrmquotatemplate_name","fsrm.ifsrmquotatemplate_name","fsrmquota/IFsrmQuotaTemplate::Name","fsrmquota/IFsrmQuotaTemplate::get_Name","fsrmquota/IFsrmQuotaTemplate::put_Name","put_Name"]
old-location: fsrm\ifsrmquotatemplate_name.htm
tech.root: fsrm
ms.assetid: 77a38b03-eb47-4298-ac13-44ffbd649752
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaTemplate interface [File Server Resource Manager],Name property, IFsrmQuotaTemplate.Name, IFsrmQuotaTemplate.put_Name, IFsrmQuotaTemplate::Name, IFsrmQuotaTemplate::get_Name, IFsrmQuotaTemplate::put_Name, Name property [File Server Resource Manager], Name property [File Server Resource Manager],IFsrmQuotaTemplate interface, fs.ifsrmquotatemplate_name, fsrm.ifsrmquotatemplate_name, fsrmquota/IFsrmQuotaTemplate::Name, fsrmquota/IFsrmQuotaTemplate::get_Name, fsrmquota/IFsrmQuotaTemplate::put_Name, put_Name
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
 - IFsrmQuotaTemplate::put_Name
 - fsrmquota/IFsrmQuotaTemplate::put_Name
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
 - IFsrmQuotaTemplate.Name
 - IFsrmQuotaTemplate.get_Name
 - IFsrmQuotaTemplate.put_Name
---

# IFsrmQuotaTemplate::put_Name


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves and sets the name of the quota template.

This property is read/write.

## -parameters

## -remarks

If you do not specify a name, FSRM generates a unique name that begins with 
    "QuotaTemplate".


#### Examples

For an example, see <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotatemplate">IFsrmQuotaTemplate</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
