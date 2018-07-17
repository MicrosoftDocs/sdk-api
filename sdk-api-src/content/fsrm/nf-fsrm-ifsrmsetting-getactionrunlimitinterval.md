---
UID: NF:fsrm.IFsrmSetting.GetActionRunLimitInterval
title: IFsrmSetting::GetActionRunLimitInterval
author: windows-sdk-content
description: Gets the time that an action that uses the global run limit interval must wait before the action is run again.
old-location: fsrm\ifsrmsetting_getactionrunlimitinterval.htm
old-project: Fsrm
ms.assetid: cbcd5532-4077-4a5c-94d4-e1fb636e6dda
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],GetActionRunLimitInterval method, GetActionRunLimitInterval, GetActionRunLimitInterval method [File Server Resource Manager], GetActionRunLimitInterval method [File Server Resource Manager],FsrmSetting class, GetActionRunLimitInterval method [File Server Resource Manager],IFsrmSetting interface, IFsrmSetting interface [File Server Resource Manager],GetActionRunLimitInterval method, IFsrmSetting.GetActionRunLimitInterval, IFsrmSetting::GetActionRunLimitInterval, fs.ifsrmsetting_getactionrunlimitinterval, fsrm.ifsrmsetting_getactionrunlimitinterval, fsrm/IFsrmSetting::GetActionRunLimitInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: FILTERED_DATA_SOURCES
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
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmSetting::GetActionRunLimitInterval


## -description


Gets the time that an action that uses the global run limit interval must wait before the action is run again.


## -parameters




### -param actionType [in]

The action type to limit. For possible values, see the <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.


### -param delayTimeMinutes [out]

The run limit interval, in minutes, that is used for the action.


## -returns



Returns the following return values:




## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

