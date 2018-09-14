---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaUsed
title: IFsrmQuota::get_QuotaUsed
author: windows-sdk-content
description: Retrieves the current amount of disk space usage charged to this quota.
old-location: fsrm\ifsrmquota_quotaused.htm
tech.root: fsrm
ms.assetid: c6df9842-9d69-4422-a8bc-c541ae31f21d
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaUsed property, IFsrmQuota.QuotaUsed, IFsrmQuota.get_QuotaUsed, IFsrmQuota::QuotaUsed, IFsrmQuota::get_QuotaUsed, QuotaUsed property [File Server Resource Manager], QuotaUsed property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotaused, fsrm.ifsrmquota_quotaused, fsrmquota/IFsrmQuota::QuotaUsed, fsrmquota/IFsrmQuota::get_QuotaUsed, get_QuotaUsed
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
 - IFsrmQuota.QuotaUsed
 - IFsrmQuota.get_QuotaUsed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuota::get_QuotaUsed


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the current amount of disk space usage charged to this quota.

This property is read-only.


## -parameters


## -remarks



The value is the total disk space usage for the directory and all its subdirectories (recursively). Files, 
    directories, streams, metadata, and other file system–specific means of persisting data are 
    used in determining the usage.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/7b755410-5520-4933-8859-9c201cbd13eb">Getting Current Usage Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

