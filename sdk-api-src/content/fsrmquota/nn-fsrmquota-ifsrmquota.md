---
UID: NN:fsrmquota.IFsrmQuota
title: IFsrmQuota (fsrmquota.h)
description: Used to define a quota for a specified directory and to retrieve use statistics.
helpviewer_keywords: ["IFsrmQuota","IFsrmQuota interface [File Server Resource Manager]","IFsrmQuota interface [File Server Resource Manager]","described","fs.ifsrmquota","fsrm.ifsrmquota","fsrm/IFsrmQuota"]
old-location: fsrm\ifsrmquota.htm
tech.root: fsrm
ms.assetid: 91ced22a-01b9-4fcf-b61a-c99e6f0286f3
ms.date: 12/05/2018
ms.keywords: IFsrmQuota, IFsrmQuota interface [File Server Resource Manager], IFsrmQuota interface [File Server Resource Manager],described, fs.ifsrmquota, fsrm.ifsrmquota, fsrm/IFsrmQuota
req.header: fsrmquota.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmQuota
 - fsrmquota/IFsrmQuota
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
 - IFsrmQuota
---

# IFsrmQuota interface


## -description

<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Used to define a quota for a specified directory and to retrieve use statistics. 

To create this interface, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-createquota">IFsrmQuotaManager::CreateQuota</a> method.

The following methods return this interface:
<ul>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumeffectivequotas">IFsrmQuotaManager::EnumEffectiveQuotas</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-enumquotas">IFsrmQuotaManager::EnumQuotas</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getquota">IFsrmQuotaManager::GetQuota</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotamanager-getrestrictivequota">IFsrmQuotaManager::GetRestrictiveQuota</a>
</li>
</ul>

## -inheritance

The <b>IFsrmQuota</b> interface inherits from <a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>. <b>IFsrmQuota</b> also has these types of members:

## -remarks

A quota limits the amount of data that the system or any user can store in a directory.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotaobject">IFsrmQuotaObject</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
