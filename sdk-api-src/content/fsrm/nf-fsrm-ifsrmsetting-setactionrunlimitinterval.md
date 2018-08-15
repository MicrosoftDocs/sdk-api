---
UID: NF:fsrm.IFsrmSetting.SetActionRunLimitInterval
title: IFsrmSetting::SetActionRunLimitInterval
author: windows-sdk-content
description: Sets the time that an action that uses the global run limit interval must wait before the action is run again.
old-location: fsrm\ifsrmsetting_setactionrunlimitinterval.htm
old-project: fsrm
ms.assetid: 4cd4d583-2906-4ba0-b113-c21db143dec2
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: FsrmSetting class [File Server Resource Manager],SetActionRunLimitInterval method, IFsrmSetting interface [File Server Resource Manager],SetActionRunLimitInterval method, IFsrmSetting.SetActionRunLimitInterval, IFsrmSetting::SetActionRunLimitInterval, SetActionRunLimitInterval, SetActionRunLimitInterval method [File Server Resource Manager], SetActionRunLimitInterval method [File Server Resource Manager],FsrmSetting class, SetActionRunLimitInterval method [File Server Resource Manager],IFsrmSetting interface, fs.ifsrmsetting_setactionrunlimitinterval, fsrm.ifsrmsetting_setactionrunlimitinterval, fsrm/IFsrmSetting::SetActionRunLimitInterval
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.redist: 
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
 - IFsrmSetting.SetActionRunLimitInterval
 - FsrmSetting.SetActionRunLimitInterval
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmSetting::SetActionRunLimitInterval


## -description


Sets the time that an action that uses the global run limit interval must wait before the action is run again.


## -parameters




### -param actionType [in]

The action type to limit. For possible values, see the <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.


### -param delayTimeMinutes [in]

The run limit interval, in minutes, to use for the action. The default is 60 minutes.


## -returns



The method returns the following return values.




## -remarks



Applies to actions that have the <a href="https://msdn.microsoft.com/3d5be77f-282f-479d-aa34-a8cb1c771951">IFsrmAction::RunLimitInterval</a> property set to –1.

This property specifies the interval that should occur before the action is run again if the global run limit interval is used. For example, if the interval has expired since the action last ran, the server will run the action again in response to an event; otherwise, the server cannot run the action again.




## -see-also




<a href="https://msdn.microsoft.com/0c27393a-9a84-4147-a7e0-582c0bf2d918">FsrmSetting</a>



<a href="https://msdn.microsoft.com/432fbaaa-7ddb-4d8c-bfbe-40cd26b08f9b">IFsrmSetting</a>
 

 

