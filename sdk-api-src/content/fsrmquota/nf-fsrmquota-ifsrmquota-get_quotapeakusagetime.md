---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaPeakUsageTime
title: IFsrmQuota::get_QuotaPeakUsageTime (fsrmquota.h)
description: Retrieves the date and time that the IFsrmQuota::QuotaPeakUsage property was set.
helpviewer_keywords: ["IFsrmQuota interface [File Server Resource Manager]","QuotaPeakUsageTime property","IFsrmQuota.QuotaPeakUsageTime","IFsrmQuota.get_QuotaPeakUsageTime","IFsrmQuota::QuotaPeakUsageTime","IFsrmQuota::get_QuotaPeakUsageTime","QuotaPeakUsageTime property [File Server Resource Manager]","QuotaPeakUsageTime property [File Server Resource Manager]","IFsrmQuota interface","fs.ifsrmquota_quotapeakusagetime","fsrm.ifsrmquota_quotapeakusagetime","fsrmquota/IFsrmQuota::QuotaPeakUsageTime","fsrmquota/IFsrmQuota::get_QuotaPeakUsageTime","get_QuotaPeakUsageTime"]
old-location: fsrm\ifsrmquota_quotapeakusagetime.htm
tech.root: fsrm
ms.assetid: 08b7c438-6bcf-4323-ac27-7e3c79c062da
ms.date: 12/05/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaPeakUsageTime property, IFsrmQuota.QuotaPeakUsageTime, IFsrmQuota.get_QuotaPeakUsageTime, IFsrmQuota::QuotaPeakUsageTime, IFsrmQuota::get_QuotaPeakUsageTime, QuotaPeakUsageTime property [File Server Resource Manager], QuotaPeakUsageTime property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotapeakusagetime, fsrm.ifsrmquota_quotapeakusagetime, fsrmquota/IFsrmQuota::QuotaPeakUsageTime, fsrmquota/IFsrmQuota::get_QuotaPeakUsageTime, get_QuotaPeakUsageTime
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
 - IFsrmQuota::get_QuotaPeakUsageTime
 - fsrmquota/IFsrmQuota::get_QuotaPeakUsageTime
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
 - IFsrmQuota.QuotaPeakUsageTime
 - IFsrmQuota.get_QuotaPeakUsageTime
---

# IFsrmQuota::get_QuotaPeakUsageTime


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the date and time that the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-get_quotapeakusage">IFsrmQuota::QuotaPeakUsage</a> property was 
    set.

This property is read-only.

## -parameters

## -remarks

The time stamp is set when the quota usage reaches a new, higher peak level, or the peak usage value is 
    reset.

To get the highest peak usage value, access the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquota-get_quotapeakusage">QuotaPeakUsage</a> property.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/getting-current-usage-values">Getting Current Usage Values</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>