---
UID: NF:fsrmquota.IFsrmQuota.get_QuotaPeakUsageTime
title: IFsrmQuota::get_QuotaPeakUsageTime
author: windows-sdk-content
description: Retrieves the date and time that the IFsrmQuota::QuotaPeakUsage property was set.
old-location: fsrm\ifsrmquota_quotapeakusagetime.htm
old-project: fsrm
ms.assetid: 08b7c438-6bcf-4323-ac27-7e3c79c062da
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IFsrmQuota interface [File Server Resource Manager],QuotaPeakUsageTime property, IFsrmQuota.QuotaPeakUsageTime, IFsrmQuota.get_QuotaPeakUsageTime, IFsrmQuota::QuotaPeakUsageTime, IFsrmQuota::get_QuotaPeakUsageTime, QuotaPeakUsageTime property [File Server Resource Manager], QuotaPeakUsageTime property [File Server Resource Manager],IFsrmQuota interface, fs.ifsrmquota_quotapeakusagetime, fsrm.ifsrmquota_quotapeakusagetime, fsrmquota/IFsrmQuota::QuotaPeakUsageTime, fsrmquota/IFsrmQuota::get_QuotaPeakUsageTime, get_QuotaPeakUsageTime
ms.prod: windows
ms.technology: windows-sdk
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
 - IFsrmQuota.QuotaPeakUsageTime
 - IFsrmQuota.get_QuotaPeakUsageTime
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuota::get_QuotaPeakUsageTime


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves the date and time that the 
    <a href="https://msdn.microsoft.com/86e2f8a1-766e-494d-9b99-c55e51d8509c">IFsrmQuota::QuotaPeakUsage</a> property was 
    set.

This property is read-only.


## -parameters


## -remarks



The time stamp is set when the quota usage reaches a new, higher peak level, or the peak usage value is 
    reset.

To get the highest peak usage value, access the 
    <a href="https://msdn.microsoft.com/86e2f8a1-766e-494d-9b99-c55e51d8509c">QuotaPeakUsage</a> property.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/7b755410-5520-4933-8859-9c201cbd13eb">Getting Current Usage Values</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91ced22a-01b9-4fcf-b61a-c99e6f0286f3">IFsrmQuota</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

