---
UID: NF:fsrmquota.IFsrmQuotaBase.AddThreshold
title: IFsrmQuotaBase::AddThreshold
author: windows-sdk-content
description: Adds a threshold to the quota object.
old-location: fsrm\ifsrmquotabase_addthreshold.htm
tech.root: fsrm
ms.assetid: 9571e169-01a3-4b72-bc84-2f9b2609a6e2
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: AddThreshold, AddThreshold method [File Server Resource Manager], AddThreshold method [File Server Resource Manager],IFsrmQuotaBase interface, IFsrmQuotaBase interface [File Server Resource Manager],AddThreshold method, IFsrmQuotaBase.AddThreshold, IFsrmQuotaBase::AddThreshold, fs.ifsrmquotabase_addthreshold, fsrm.ifsrmquotabase_addthreshold, fsrmquota/IFsrmQuotaBase::AddThreshold
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
 - IFsrmQuotaBase.AddThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaBase::AddThreshold


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Adds a threshold to the quota object.


## -parameters




### -param threshold [in]

The threshold to add to the quota object. The threshold is expressed as a percentage of the 
      <a href="https://msdn.microsoft.com/2f2b5d8f-70b7-497e-9c51-171dca657c69">quota limit</a>. The value must be from 1 through 
      250, inclusively.


## -returns



The method returns the following return values.




## -remarks



You can specify up to 16 unique thresholds for a quota.

A threshold defines the percentage (as a whole number) of directory quota limit used. When the size of all 
    data in the directory exceeds the threshold, the FSRM server performs the specified actions (see 
    <a href="https://msdn.microsoft.com/27813041-ee42-4412-982e-fce594c5e648">IFsrmQuotaBase::CreateThresholdAction</a>).


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/88ff3968-cb83-4b66-83e9-a58205b4be82">Using Templates to Define Quotas</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

