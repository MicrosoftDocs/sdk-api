---
UID: NF:fsrmquota.IFsrmQuotaBase.CreateThresholdAction
title: IFsrmQuotaBase::CreateThresholdAction (fsrmquota.h)
author: windows-sdk-content
description: Creates an action and associates it with the specified threshold.
old-location: fsrm\ifsrmquotabase_createthresholdaction.htm
tech.root: fsrm
ms.assetid: 27813041-ee42-4412-982e-fce594c5e648
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateThresholdAction, CreateThresholdAction method [File Server Resource Manager], CreateThresholdAction method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],CreateThresholdAction method, IFsrmQuotaBase.CreateThresholdAction, IFsrmQuotaBase::CreateThresholdAction, fs.ifsrmquotabase_createthresholdaction, fsrm.ifsrmquotabase_createthresholdaction, fsrmquota/IFsrmQuotaBase::CreateThresholdAction
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaBase.CreateThresholdAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaBase::CreateThresholdAction


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Creates an action and associates it with the specified threshold.


## -parameters




### -param threshold [in]

The threshold with which to associate the action. Specify the same value that you specified when calling 
      the <a href="https://msdn.microsoft.com/9571e169-01a3-4b72-bc84-2f9b2609a6e2">IFsrmQuotaBase::AddThreshold</a> 
      method.


### -param actionType [in]

The action to perform when the threshold is reached or exceeded. For possible values, see the 
      <a href="https://msdn.microsoft.com/3e34395e-b8e6-4288-a040-dff6cf7f5fe6">FsrmActionType</a> enumeration.


### -param action [out]

An <a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a> interface of the newly created action. 
      Query the interface for the action interface that you specified in the <i>actionType</i> 
      parameter. For example, if the action type is <b>FsrmActionType_Command</b>, query the 
      interface for the <a href="https://msdn.microsoft.com/b7f9fc8c-2f55-4a0e-879a-64c368abcabb">IFsrmActionCommand</a> interface.


## -returns



The method returns the following return values.




## -remarks



You can specify up to four unique actions for each threshold.

The action is deleted if the threshold is deleted.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/88ff3968-cb83-4b66-83e9-a58205b4be82">Using Templates to Define Quotas</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

