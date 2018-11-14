---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaPeakUsage
title: IFsrmQuota::get_QuotaPeakUsage
author: windows-sdk-content
description: Retrieves the highest amount of disk space usage charged to this quota.
old-location: fsrm\ifsrmquota_quotapeakusage.htm
tech.root: Fsrm
ms.assetid: 86e2f8a1-766e-494d-9b99-c55e51d8509c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaPeakUsage property, IFsrmQuota.QuotaPeakUsage, IFsrmQuota.get_QuotaPeakUsage, IFsrmQuota::QuotaPeakUsage, IFsrmQuota::get_QuotaPeakUsage, QuotaPeakUsage property [File Server Resource Manager], QuotaPeakUsage property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotapeakusage, fsrm.ifsrmquota_quotapeakusage, fsrmquota/IFsrmQuota::QuotaPeakUsage, fsrmquota/IFsrmQuota::get_QuotaPeakUsage, get_QuotaPeakUsage
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
 - IFsrmQuota.QuotaPeakUsage
 - IFsrmQuota.get_QuotaPeakUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- fsrmquota.h
: 
- IFsrmQuota.get_QuotaPeakUsage
: 
---

# IFsrmQuota::get_QuotaPeakUsage


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the highest amount of disk space usage charged to this quota.

This property is read-only.


## -parameters


## -remarks



The value represents the highest amount of disk space charged to this quota since the last call to 
    <a href="https://msdn.microsoft.com/5c2b18a9-912a-49cc-bf4f-07f172a328b1">IFsrmQuota::ResetPeakUsage</a>. To reset this value, 
    call the <b>ResetPeakUsage</b> method.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/7b755410-5520-4933-8859-9c201cbd13eb">Getting Current Usage Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

