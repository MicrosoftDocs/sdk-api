---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaPeakUsage
title: IFsrmQuota::get_QuotaPeakUsage (fsrmquota.h)
description: Retrieves the highest amount of disk space usage charged to this quota.
helpviewer_keywords: ["IFsrmQuota interface [File Server Resource Manager]","QuotaPeakUsage property","IFsrmQuota.QuotaPeakUsage","IFsrmQuota.get_QuotaPeakUsage","IFsrmQuota::QuotaPeakUsage","IFsrmQuota::get_QuotaPeakUsage","QuotaPeakUsage property [File Server Resource Manager]","QuotaPeakUsage property [File Server Resource Manager]","IFsrmQuota interface","fs.ifsrmquota_quotapeakusage","fsrm.ifsrmquota_quotapeakusage","fsrmquota/IFsrmQuota::QuotaPeakUsage","fsrmquota/IFsrmQuota::get_QuotaPeakUsage","get_QuotaPeakUsage"]
old-location: fsrm\ifsrmquota_quotapeakusage.htm
tech.root: fsrm
ms.assetid: 86e2f8a1-766e-494d-9b99-c55e51d8509c
ms.date: 12/05/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaPeakUsage property, IFsrmQuota.QuotaPeakUsage, IFsrmQuota.get_QuotaPeakUsage, IFsrmQuota::QuotaPeakUsage, IFsrmQuota::get_QuotaPeakUsage, QuotaPeakUsage property [File Server Resource Manager], QuotaPeakUsage property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotapeakusage, fsrm.ifsrmquota_quotapeakusage, fsrmquota/IFsrmQuota::QuotaPeakUsage, fsrmquota/IFsrmQuota::get_QuotaPeakUsage, get_QuotaPeakUsage
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
 - IFsrmQuota::get_QuotaPeakUsage
 - fsrmquota/IFsrmQuota::get_QuotaPeakUsage
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
 - IFsrmQuota.QuotaPeakUsage
 - IFsrmQuota.get_QuotaPeakUsage
---

# IFsrmQuota::get_QuotaPeakUsage


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the highest amount of disk space usage charged to this quota.

This property is read-only.

## -parameters

## -remarks

The value represents the highest amount of disk space charged to this quota since the last call to 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-resetpeakusage">IFsrmQuota::ResetPeakUsage</a>. To reset this value, 
    call the <b>ResetPeakUsage</b> method.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/getting-current-usage-values">Getting Current Usage Values</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>