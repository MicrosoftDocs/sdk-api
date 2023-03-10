---
UID: NF:fsrmquota.IFsrmQuotaBase.DeleteThreshold
title: IFsrmQuotaBase::DeleteThreshold (fsrmquota.h)
description: Deletes a threshold from the quota object.
helpviewer_keywords: ["DeleteThreshold","DeleteThreshold method [File Server Resource Manager]","DeleteThreshold method [File Server Resource Manager]","IFsrmQuotaBase interface","IFsrmQuotaBase interface [File Server Resource Manager]","DeleteThreshold method","IFsrmQuotaBase.DeleteThreshold","IFsrmQuotaBase::DeleteThreshold","fs.ifsrmquotabase_deletethreshold","fsrm.ifsrmquotabase_deletethreshold","fsrmquota/IFsrmQuotaBase::DeleteThreshold"]
old-location: fsrm\ifsrmquotabase_deletethreshold.htm
tech.root: fsrm
ms.assetid: 6f6ace15-05aa-4276-88eb-3a4315b3b51c
ms.date: 12/05/2018
ms.keywords: DeleteThreshold, DeleteThreshold method [File Server Resource Manager], DeleteThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],DeleteThreshold method, IFsrmQuotaBase.DeleteThreshold, IFsrmQuotaBase::DeleteThreshold, fs.ifsrmquotabase_deletethreshold, fsrm.ifsrmquotabase_deletethreshold, fsrmquota/IFsrmQuotaBase::DeleteThreshold
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
 - IFsrmQuotaBase::DeleteThreshold
 - fsrmquota/IFsrmQuotaBase::DeleteThreshold
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
 - IFsrmQuotaBase.DeleteThreshold
---

# IFsrmQuotaBase::DeleteThreshold


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Deletes a threshold from the quota object.

## -parameters

### -param threshold [in]

The threshold to delete.

## -returns

The method returns the following return values.

## -remarks

All the actions associated with the threshold are also deleted. Note that the actions are not deleted until 
    the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmQuotaBase::Commit</a> method is called.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>