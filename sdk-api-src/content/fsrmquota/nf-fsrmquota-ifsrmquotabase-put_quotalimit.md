---
UID: NF:fsrmquota.IFsrmQuotaBase.put_QuotaLimit
title: IFsrmQuotaBase::put_QuotaLimit (fsrmquota.h)
description: Retrieves or sets the quota limit for the object. (Put)
helpviewer_keywords: ["IFsrmQuotaBase interface [File Server Resource Manager]","QuotaLimit property","IFsrmQuotaBase.QuotaLimit","IFsrmQuotaBase.put_QuotaLimit","IFsrmQuotaBase::QuotaLimit","IFsrmQuotaBase::get_QuotaLimit","IFsrmQuotaBase::put_QuotaLimit","QuotaLimit property [File Server Resource Manager]","QuotaLimit property [File Server Resource Manager]","IFsrmQuotaBase interface","fs.ifsrmquotabase_quotalimit","fsrm.ifsrmquotabase_quotalimit","fsrmquota/IFsrmQuotaBase::QuotaLimit","fsrmquota/IFsrmQuotaBase::get_QuotaLimit","fsrmquota/IFsrmQuotaBase::put_QuotaLimit","put_QuotaLimit"]
old-location: fsrm\ifsrmquotabase_quotalimit.htm
tech.root: fsrm
ms.assetid: 2f2b5d8f-70b7-497e-9c51-171dca657c69
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaBase interface [File Server Resource Manager],QuotaLimit property, IFsrmQuotaBase.QuotaLimit, IFsrmQuotaBase.put_QuotaLimit, IFsrmQuotaBase::QuotaLimit, IFsrmQuotaBase::get_QuotaLimit, IFsrmQuotaBase::put_QuotaLimit, QuotaLimit property [File Server Resource Manager], QuotaLimit property [File Server Resource Manager],IFsrmQuotaBase interface, fs.ifsrmquotabase_quotalimit, fsrm.ifsrmquotabase_quotalimit, fsrmquota/IFsrmQuotaBase::QuotaLimit, fsrmquota/IFsrmQuotaBase::get_QuotaLimit, fsrmquota/IFsrmQuotaBase::put_QuotaLimit, put_QuotaLimit
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
 - IFsrmQuotaBase::put_QuotaLimit
 - fsrmquota/IFsrmQuotaBase::put_QuotaLimit
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
 - IFsrmQuotaBase.QuotaLimit
 - IFsrmQuotaBase.get_QuotaLimit
 - IFsrmQuotaBase.put_QuotaLimit
---

# IFsrmQuotaBase::put_QuotaLimit


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves or sets the quota limit for the object.

This property is read/write.

## -parameters

## -remarks

If the quota limit is enforced, an IO operation that exceeds the limit will fail.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
