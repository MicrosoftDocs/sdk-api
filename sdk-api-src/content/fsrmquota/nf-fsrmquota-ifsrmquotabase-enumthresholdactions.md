---
UID: NF:fsrmquota.IFsrmQuotaBase.EnumThresholdActions
title: IFsrmQuotaBase::EnumThresholdActions (fsrmquota.h)
description: Enumerates all the actions for the specified threshold.
helpviewer_keywords: ["EnumThresholdActions","EnumThresholdActions method [File Server Resource Manager]","EnumThresholdActions method [File Server Resource Manager]","IFsrmQuotaBase interface","IFsrmQuotaBase interface [File Server Resource Manager]","EnumThresholdActions method","IFsrmQuotaBase.EnumThresholdActions","IFsrmQuotaBase::EnumThresholdActions","fs.ifsrmquotabase_enumthresholdactions","fsrm.ifsrmquotabase_enumthresholdactions","fsrmquota/IFsrmQuotaBase::EnumThresholdActions"]
old-location: fsrm\ifsrmquotabase_enumthresholdactions.htm
tech.root: fsrm
ms.assetid: ce4f85a9-f2e0-42df-adb4-7c21256d5305
ms.date: 12/05/2018
ms.keywords: EnumThresholdActions, EnumThresholdActions method [File Server Resource Manager], EnumThresholdActions method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],EnumThresholdActions method, IFsrmQuotaBase.EnumThresholdActions, IFsrmQuotaBase::EnumThresholdActions, fs.ifsrmquotabase_enumthresholdactions, fsrm.ifsrmquotabase_enumthresholdactions, fsrmquota/IFsrmQuotaBase::EnumThresholdActions
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
 - IFsrmQuotaBase::EnumThresholdActions
 - fsrmquota/IFsrmQuotaBase::EnumThresholdActions
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
 - IFsrmQuotaBase.EnumThresholdActions
---

# IFsrmQuotaBase::EnumThresholdActions


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Enumerates all the actions for the specified threshold.

## -parameters

### -param threshold [in]

The threshold that contains the actions that you want to enumerate.

### -param actions [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcollection">IFsrmCollection</a> interface that contains a 
      collection of actions. The variant type of each item in the collection is <b>VT_DISPATCH</b>. 
      Query the <b>pdispVal</b> member of the variant to get an 
      <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a> interface. You can use the 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_actiontype">IFsrmAction::ActionType</a> property to determine 
      the actual action interface to query.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>