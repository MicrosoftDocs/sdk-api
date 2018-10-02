---
UID: NF:fsrmquota.IFsrmQuotaBase.DeleteThreshold
title: IFsrmQuotaBase::DeleteThreshold
author: windows-sdk-content
description: Deletes a threshold from the quota object.
old-location: fsrm\ifsrmquotabase_deletethreshold.htm
tech.root: Fsrm
ms.assetid: 6f6ace15-05aa-4276-88eb-3a4315b3b51c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteThreshold, DeleteThreshold method [File Server Resource Manager], DeleteThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],DeleteThreshold method, IFsrmQuotaBase.DeleteThreshold, IFsrmQuotaBase::DeleteThreshold, fs.ifsrmquotabase_deletethreshold, fsrm.ifsrmquotabase_deletethreshold, fsrmquota/IFsrmQuotaBase::DeleteThreshold
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IFsrmQuotaBase.DeleteThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaBase::DeleteThreshold


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Deletes a threshold from the quota object.


## -parameters




### -param threshold [in]

The threshold to delete.


## -returns



The method returns the following return values.




## -remarks



All the actions associated with the threshold are also deleted. Note that the actions are not deleted until 
    the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmQuotaBase::Commit</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

