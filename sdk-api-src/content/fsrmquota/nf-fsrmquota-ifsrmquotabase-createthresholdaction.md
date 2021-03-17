---
UID: NF:fsrmquota.IFsrmQuotaBase.CreateThresholdAction
title: IFsrmQuotaBase::CreateThresholdAction (fsrmquota.h)
description: Creates an action and associates it with the specified threshold.
helpviewer_keywords: ["CreateThresholdAction","CreateThresholdAction method [File Server Resource Manager]","CreateThresholdAction method [File Server Resource Manager]","IFsrmQuotaBase interface","IFsrmQuotaBase interface [File Server Resource Manager]","CreateThresholdAction method","IFsrmQuotaBase.CreateThresholdAction","IFsrmQuotaBase::CreateThresholdAction","fs.ifsrmquotabase_createthresholdaction","fsrm.ifsrmquotabase_createthresholdaction","fsrmquota/IFsrmQuotaBase::CreateThresholdAction"]
old-location: fsrm\ifsrmquotabase_createthresholdaction.htm
tech.root: fsrm
ms.assetid: 27813041-ee42-4412-982e-fce594c5e648
ms.date: 12/05/2018
ms.keywords: CreateThresholdAction, CreateThresholdAction method [File Server Resource Manager], CreateThresholdAction method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],CreateThresholdAction method, IFsrmQuotaBase.CreateThresholdAction, IFsrmQuotaBase::CreateThresholdAction, fs.ifsrmquotabase_createthresholdaction, fsrm.ifsrmquotabase_createthresholdaction, fsrmquota/IFsrmQuotaBase::CreateThresholdAction
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
 - IFsrmQuotaBase::CreateThresholdAction
 - fsrmquota/IFsrmQuotaBase::CreateThresholdAction
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
 - IFsrmQuotaBase.CreateThresholdAction
---

# IFsrmQuotaBase::CreateThresholdAction


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Creates an action and associates it with the specified threshold.

## -parameters

### -param threshold [in]

The threshold with which to associate the action. Specify the same value that you specified when calling 
      the <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-addthreshold">IFsrmQuotaBase::AddThreshold</a> 
      method.

### -param actionType [in]

The action to perform when the threshold is reached or exceeded. For possible values, see the 
      <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a> enumeration.

### -param action [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface of the newly created action. 
      Query the interface for the action interface that you specified in the <i>actionType</i> 
      parameter. For example, if the action type is <b>FsrmActionType_Command</b>, query the 
      interface for the <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmactioncommand">IFsrmActionCommand</a> interface.

## -returns

The method returns the following return values.

## -remarks

You can specify up to four unique actions for each threshold.

The action is deleted if the threshold is deleted.


#### Examples

For an example, see 
     <a href="/previous-versions/windows/desktop/fsrm/using-templates-to-define-quotas">Using Templates to Define Quotas</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>