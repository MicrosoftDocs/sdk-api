---
UID: NF:fsrmquota.IFsrmQuotaBase.AddThreshold
title: IFsrmQuotaBase::AddThreshold (fsrmquota.h)
description: Adds a threshold to the quota object.
helpviewer_keywords: ["AddThreshold","AddThreshold method [File Server Resource Manager]","AddThreshold method [File Server Resource Manager]","IFsrmQuotaBase interface","IFsrmQuotaBase interface [File Server Resource Manager]","AddThreshold method","IFsrmQuotaBase.AddThreshold","IFsrmQuotaBase::AddThreshold","fs.ifsrmquotabase_addthreshold","fsrm.ifsrmquotabase_addthreshold","fsrmquota/IFsrmQuotaBase::AddThreshold"]
old-location: fsrm\ifsrmquotabase_addthreshold.htm
tech.root: fsrm
ms.assetid: 9571e169-01a3-4b72-bc84-2f9b2609a6e2
ms.date: 12/05/2018
ms.keywords: AddThreshold, AddThreshold method [File Server Resource Manager], AddThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],AddThreshold method, IFsrmQuotaBase.AddThreshold, IFsrmQuotaBase::AddThreshold, fs.ifsrmquotabase_addthreshold, fsrm.ifsrmquotabase_addthreshold, fsrmquota/IFsrmQuotaBase::AddThreshold
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
 - IFsrmQuotaBase::AddThreshold
 - fsrmquota/IFsrmQuotaBase::AddThreshold
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
 - IFsrmQuotaBase.AddThreshold
---

# IFsrmQuotaBase::AddThreshold


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Adds a threshold to the quota object.

## -parameters

### -param threshold [in]

The threshold to add to the quota object. The threshold is expressed as a percentage of the 
      <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-get_quotalimit">quota limit</a>. The value must be from 1 through 
      250, inclusively.

## -returns

The method returns the following return values.

## -remarks

You can specify up to 16 unique thresholds for a quota.

A threshold defines the percentage (as a whole number) of directory quota limit used. When the size of all 
    data in the directory exceeds the threshold, the FSRM server performs the specified actions (see 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-createthresholdaction">IFsrmQuotaBase::CreateThresholdAction</a>).


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>