---
UID: NF:fsrm.IFsrmSetting.SetActionRunLimitInterval
title: IFsrmSetting::SetActionRunLimitInterval (fsrm.h)
description: Sets the time that an action that uses the global run limit interval must wait before the action is run again.
helpviewer_keywords: ["FsrmSetting class [File Server Resource Manager]","SetActionRunLimitInterval method","IFsrmSetting interface [File Server Resource Manager]","SetActionRunLimitInterval method","IFsrmSetting.SetActionRunLimitInterval","IFsrmSetting::SetActionRunLimitInterval","SetActionRunLimitInterval","SetActionRunLimitInterval method [File Server Resource Manager]","SetActionRunLimitInterval method [File Server Resource Manager]","FsrmSetting class","SetActionRunLimitInterval method [File Server Resource Manager]","IFsrmSetting interface","fs.ifsrmsetting_setactionrunlimitinterval","fsrm.ifsrmsetting_setactionrunlimitinterval","fsrm/IFsrmSetting::SetActionRunLimitInterval"]
old-location: fsrm\ifsrmsetting_setactionrunlimitinterval.htm
tech.root: fsrm
ms.assetid: 4cd4d583-2906-4ba0-b113-c21db143dec2
ms.date: 12/05/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],SetActionRunLimitInterval method, IFsrmSetting interface [File Server Resource Manager],SetActionRunLimitInterval method, IFsrmSetting.SetActionRunLimitInterval, IFsrmSetting::SetActionRunLimitInterval, SetActionRunLimitInterval, SetActionRunLimitInterval method [File Server Resource Manager], SetActionRunLimitInterval method [File Server Resource Manager],FsrmSetting class, SetActionRunLimitInterval method [File Server Resource Manager],IFsrmSetting interface, fs.ifsrmsetting_setactionrunlimitinterval, fsrm.ifsrmsetting_setactionrunlimitinterval, fsrm/IFsrmSetting::SetActionRunLimitInterval
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
 - IFsrmSetting::SetActionRunLimitInterval
 - fsrm/IFsrmSetting::SetActionRunLimitInterval
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
 - IFsrmSetting.SetActionRunLimitInterval
 - FsrmSetting.SetActionRunLimitInterval
---

# IFsrmSetting::SetActionRunLimitInterval


## -description

Sets the time that an action that uses the global run limit interval must wait before the action is run again.

## -parameters

### -param actionType [in]

The action type to limit. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmactiontype">FsrmActionType</a> enumeration.

### -param delayTimeMinutes [in]

The run limit interval, in minutes, to use for the action. The default is 60 minutes.

## -returns

The method returns the following return values.

## -remarks

Applies to actions that have the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmaction-get_runlimitinterval">IFsrmAction::RunLimitInterval</a> property set to –1.

This property specifies the interval that should occur before the action is run again if the global run limit interval is used. For example, if the interval has expired since the action last ran, the server will run the action again in response to an event; otherwise, the server cannot run the action again.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmsetting">FsrmSetting</a>



<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmsetting">IFsrmSetting</a>