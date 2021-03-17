---
UID: NF:fsrmquota.IFsrmQuotaBase.get_Thresholds
title: IFsrmQuotaBase::get_Thresholds (fsrmquota.h)
description: Retrieves the thresholds for the quota object.
helpviewer_keywords: ["IFsrmQuotaBase interface [File Server Resource Manager]","Thresholds property","IFsrmQuotaBase.Thresholds","IFsrmQuotaBase.get_Thresholds","IFsrmQuotaBase::Thresholds","IFsrmQuotaBase::get_Thresholds","Thresholds property [File Server Resource Manager]","Thresholds property [File Server Resource Manager]","IFsrmQuotaBase interface","fs.ifsrmquotabase_thresholds","fsrm.ifsrmquotabase_thresholds","fsrmquota/IFsrmQuotaBase::Thresholds","fsrmquota/IFsrmQuotaBase::get_Thresholds","get_Thresholds"]
old-location: fsrm\ifsrmquotabase_thresholds.htm
tech.root: fsrm
ms.assetid: e9a68b62-5d53-419f-a0c4-2e284fa51313
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaBase interface [File Server Resource Manager],Thresholds property, IFsrmQuotaBase.Thresholds, IFsrmQuotaBase.get_Thresholds, IFsrmQuotaBase::Thresholds, IFsrmQuotaBase::get_Thresholds, Thresholds property [File Server Resource Manager], Thresholds property [File Server Resource Manager],IFsrmQuotaBase interface, fs.ifsrmquotabase_thresholds, fsrm.ifsrmquotabase_thresholds, fsrmquota/IFsrmQuotaBase::Thresholds, fsrmquota/IFsrmQuotaBase::get_Thresholds, get_Thresholds
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
 - IFsrmQuotaBase::get_Thresholds
 - fsrmquota/IFsrmQuotaBase::get_Thresholds
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
 - IFsrmQuotaBase.Thresholds
 - IFsrmQuotaBase.get_Thresholds
---

# IFsrmQuotaBase::get_Thresholds


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the thresholds for the quota object.

This property is read-only.

## -parameters

## -remarks

To set a threshold, call the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-addthreshold">IFsrmQuotaBase::AddThreshold</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>