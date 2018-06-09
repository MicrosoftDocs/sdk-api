---
UID: NF:fsrmquota.IFsrmQuotaManager.CreateQuota
title: IFsrmQuotaManager::CreateQuota
author: windows-sdk-content
description: Creates a quota for the specified directory.
old-location: fsrm\ifsrmquotamanager_createquota.htm
old-project: Fsrm
ms.assetid: 09f0b952-e24f-4388-8e82-6b34145f9ad4
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateQuota, CreateQuota method [File Server Resource Manager], CreateQuota method [File Server Resource Manager],FsrmQuotaManager class, CreateQuota method [File Server Resource Manager],IFsrmQuotaManager interface, CreateQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],CreateQuota method, IFsrmQuotaManager interface [File Server Resource Manager],CreateQuota method, IFsrmQuotaManager.CreateQuota, IFsrmQuotaManager::CreateQuota, IFsrmQuotaManagerEx interface [File Server Resource Manager],CreateQuota method, IFsrmQuotaManagerEx::CreateQuota, fs.ifsrmquotamanager_createquota, fsrm.ifsrmquotamanager_createquota, fsrmquota/IFsrmQuotaManager::CreateQuota, fsrmquota/IFsrmQuotaManagerEx::CreateQuota
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmQuotaManager.CreateQuota
 - IFsrmQuotaManagerEx.CreateQuota
 - FsrmQuotaManager.CreateQuota
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaManager::CreateQuota


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Creates a quota for the specified directory.


## -parameters




### -param path [in]

The local directory path to which the quota applies. The string is limited to 260 characters.


### -param quota [out]

An <a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a> interface to the newly created quota 
      object. Use this interface to define the quota. To add the quota to FSRM, call 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmQuota::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



The quota applies to the directory and all its subdirectories (recursively). Quotas specified on directories 
    higher in the directory tree further restrict the quota specified on this directory.

If the quota specifies the <b>FsrmQuotaFlags_Enforce</b>
<a href="https://msdn.microsoft.com/af856281-8161-4165-bf24-0c160f7394d2">quota flag</a>, the file IO is blocked when the quota 
    is exceeded, but there are no actions taken, such as a command being run or a report generated. To perform actions 
    when the quota is exceeded, <a href="https://msdn.microsoft.com/9571e169-01a3-4b72-bc84-2f9b2609a6e2">create a threshold</a> 
    and specify an action to run. To perform the action when the quota is exceeded, set the threshold to 
    100 (percent).


#### Examples

For an example, see <a href="https://msdn.microsoft.com/b4471a75-f8c9-48aa-8ce3-1e998dbe6952">Defining a Quota</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a61a4797-b3f5-4f50-9b7c-6e30d4615b56">FsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

