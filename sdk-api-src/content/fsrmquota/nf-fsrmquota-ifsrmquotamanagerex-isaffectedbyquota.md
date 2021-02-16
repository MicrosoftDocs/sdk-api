---
UID: NF:fsrmquota.IFsrmQuotaManagerEx.IsAffectedByQuota
title: IFsrmQuotaManagerEx::IsAffectedByQuota (fsrmquota.h)
description: Retrieves a value that determines whether a specified path is subject to a quota.
helpviewer_keywords: ["IFsrmQuotaManagerEx interface [File Server Resource Manager]","IsAffectedByQuota method","IFsrmQuotaManagerEx.IsAffectedByQuota","IFsrmQuotaManagerEx::IsAffectedByQuota","IsAffectedByQuota","IsAffectedByQuota method [File Server Resource Manager]","IsAffectedByQuota method [File Server Resource Manager]","IFsrmQuotaManagerEx interface","fs.ifsrmquotamanagerex_isaffectedbyquota","fsrm.ifsrmquotamanagerex_isaffectedbyquota","fsrmquota/IFsrmQuotaManagerEx::IsAffectedByQuota"]
old-location: fsrm\ifsrmquotamanagerex_isaffectedbyquota.htm
tech.root: fsrm
ms.assetid: 8b366eae-5554-4c20-9ba9-c3a6e319712f
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaManagerEx interface [File Server Resource Manager],IsAffectedByQuota method, IFsrmQuotaManagerEx.IsAffectedByQuota, IFsrmQuotaManagerEx::IsAffectedByQuota, IsAffectedByQuota, IsAffectedByQuota method [File Server Resource Manager], IsAffectedByQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, fs.ifsrmquotamanagerex_isaffectedbyquota, fsrm.ifsrmquotamanagerex_isaffectedbyquota, fsrmquota/IFsrmQuotaManagerEx::IsAffectedByQuota
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmQuotaManagerEx::IsAffectedByQuota
 - fsrmquota/IFsrmQuotaManagerEx::IsAffectedByQuota
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
 - IFsrmQuotaManagerEx.IsAffectedByQuota
---

# IFsrmQuotaManagerEx::IsAffectedByQuota


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves a value that determines whether a specified path is subject to a quota.

## -parameters

### -param path [in]

The local directory path to determine whether a quota applies.

### -param options [in]

The options to use when checking for a quota. For possible values, see the 
     <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param affected [out]

Is <b>VARIANT_TRUE</b> if the path referred to by the 
     <i>path</i> parameter is subject to a quota, otherwise it is 
     <b>VARIANT_FALSE</b>.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>