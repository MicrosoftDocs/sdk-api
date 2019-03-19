---
UID: NF:fsrmquota.IFsrmQuotaBase.ModifyThreshold
title: IFsrmQuotaBase::ModifyThreshold (fsrmquota.h)
author: windows-sdk-content
description: Changes the threshold value.
old-location: fsrm\ifsrmquotabase_modifythreshold.htm
tech.root: fsrm
ms.assetid: 46cda78a-7c1d-42e0-abff-3be9c13925f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmQuotaBase interface [File Server Resource Manager],ModifyThreshold method, IFsrmQuotaBase.ModifyThreshold, IFsrmQuotaBase::ModifyThreshold, ModifyThreshold, ModifyThreshold method [File Server Resource Manager], ModifyThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, fs.ifsrmquotabase_modifythreshold, fsrm.ifsrmquotabase_modifythreshold, fsrmquota/IFsrmQuotaBase::ModifyThreshold
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
 - IFsrmQuotaBase.ModifyThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaBase::ModifyThreshold


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Changes  the threshold value.


## -parameters




### -param threshold [in]

The previous threshold value.


### -param newThreshold [in]

The new threshold value.  The value must be from 1 through 250, inclusively.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

