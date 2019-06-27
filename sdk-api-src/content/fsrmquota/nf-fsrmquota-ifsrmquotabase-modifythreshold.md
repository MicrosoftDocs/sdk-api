---
UID: NF:fsrmquota.IFsrmQuotaBase.ModifyThreshold
title: IFsrmQuotaBase::ModifyThreshold (fsrmquota.h)
author: windows-sdk-content
description: Changes the threshold value.
old-location: fsrm\ifsrmquotabase_modifythreshold.htm
tech.root: fsrm
ms.assetid: 46cda78a-7c1d-42e0-abff-3be9c13925f5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmQuotaBase interface [File Server Resource Manager],ModifyThreshold method, IFsrmQuotaBase.ModifyThreshold, IFsrmQuotaBase::ModifyThreshold, ModifyThreshold, ModifyThreshold method [File Server Resource Manager], ModifyThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, fs.ifsrmquotabase_modifythreshold, fsrm.ifsrmquotabase_modifythreshold, fsrmquota/IFsrmQuotaBase::ModifyThreshold
ms.topic: method
f1_keywords: 
 - "fsrmquota/IFsrmQuotaBase.ModifyThreshold"
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
ms.custom: 19H1
---

# IFsrmQuotaBase::ModifyThreshold


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Changes  the threshold value.


## -parameters




### -param threshold [in]

The previous threshold value.


### -param newThreshold [in]

The new threshold value.  The value must be from 1 through 250, inclusively.


## -returns



The method returns the following return values.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotabase">IFsrmQuotaBase</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
 

 

