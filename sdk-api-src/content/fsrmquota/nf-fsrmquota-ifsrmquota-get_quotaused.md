---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaUsed
title: IFsrmQuota::get_QuotaUsed (fsrmquota.h)
description: Retrieves the current amount of disk space usage charged to this quota.
helpviewer_keywords: ["IFsrmQuota interface [File Server Resource Manager]","QuotaUsed property","IFsrmQuota.QuotaUsed","IFsrmQuota.get_QuotaUsed","IFsrmQuota::QuotaUsed","IFsrmQuota::get_QuotaUsed","QuotaUsed property [File Server Resource Manager]","QuotaUsed property [File Server Resource Manager]","IFsrmQuota interface","fs.ifsrmquota_quotaused","fsrm.ifsrmquota_quotaused","fsrmquota/IFsrmQuota::QuotaUsed","fsrmquota/IFsrmQuota::get_QuotaUsed","get_QuotaUsed"]
old-location: fsrm\ifsrmquota_quotaused.htm
tech.root: fsrm
ms.assetid: c6df9842-9d69-4422-a8bc-c541ae31f21d
ms.date: 12/05/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaUsed property, IFsrmQuota.QuotaUsed, IFsrmQuota.get_QuotaUsed, IFsrmQuota::QuotaUsed, IFsrmQuota::get_QuotaUsed, QuotaUsed property [File Server Resource Manager], QuotaUsed property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotaused, fsrm.ifsrmquota_quotaused, fsrmquota/IFsrmQuota::QuotaUsed, fsrmquota/IFsrmQuota::get_QuotaUsed, get_QuotaUsed
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
 - IFsrmQuota::get_QuotaUsed
 - fsrmquota/IFsrmQuota::get_QuotaUsed
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
 - IFsrmQuota.QuotaUsed
 - IFsrmQuota.get_QuotaUsed
---

# IFsrmQuota::get_QuotaUsed


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves the current amount of disk space usage charged to this quota.

This property is read-only.

## -parameters

## -remarks

The value is the total disk space usage for the directory and all its subdirectories (recursively). Files, 
    directories, streams, metadata, and other file system–specific means of persisting data are 
    used in determining the usage.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/getting-current-usage-values">Getting Current Usage Values</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquota">IFsrmQuota</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>