---
UID: NF:fsrm.IFsrmSetting.GetActionRunLimitInterval
title: IFsrmSetting::GetActionRunLimitInterval (fsrm.h)
description: Gets the time that an action that uses the global run limit interval must wait before the action is run again.
helpviewer_keywords: ["FsrmSetting class [File Server Resource Manager]","GetActionRunLimitInterval method","GetActionRunLimitInterval","GetActionRunLimitInterval method [File Server Resource Manager]","GetActionRunLimitInterval method [File Server Resource Manager]","FsrmSetting class","GetActionRunLimitInterval method [File Server Resource Manager]","IFsrmSetting interface","IFsrmSetting interface [File Server Resource Manager]","GetActionRunLimitInterval method","IFsrmSetting.GetActionRunLimitInterval","IFsrmSetting::GetActionRunLimitInterval","fs.ifsrmsetting_getactionrunlimitinterval","fsrm.ifsrmsetting_getactionrunlimitinterval","fsrm/IFsrmSetting::GetActionRunLimitInterval"]
old-location: fsrm\ifsrmsetting_getactionrunlimitinterval.htm
tech.root: fsrm
ms.assetid: cbcd5532-4077-4a5c-94d4-e1fb636e6dda
ms.date: 12/05/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],GetActionRunLimitInterval method, GetActionRunLimitInterval, GetActionRunLimitInterval method [File Server Resource Manager], GetActionRunLimitInterval method [File Server Resource Manager],FsrmSetting class, GetActionRunLimitInterval method [File Server Resource Manager],IFsrmSetting interface, IFsrmSetting interface [File Server Resource Manager],GetActionRunLimitInterval method, IFsrmSetting.GetActionRunLimitInterval, IFsrmSetting::GetActionRunLimitInterval, fs.ifsrmsetting_getactionrunlimitinterval, fsrm.ifsrmsetting_getactionrunlimitinterval, fsrm/IFsrmSetting::GetActionRunLimitInterval
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmSetting::GetActionRunLimitInterval
 - fsrm/IFsrmSetting::GetActionRunLimitInterval
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
 - IFsrmSetting.GetActionRunLimitInterval
 - FsrmSetting.GetActionRunLimitInterval
---

# IFsrmSetting::GetActionRunLimitInterval


## -description

Gets the time that an action that uses the global run limit interval must wait before the action is run again.

## -parameters

### -param actionType [in]

The action type to limit. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a> enumeration.

### -param delayTimeMinutes [out]

The run limit interval, in minutes, that is used for the action.

## -returns

Returns the following return values:

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>