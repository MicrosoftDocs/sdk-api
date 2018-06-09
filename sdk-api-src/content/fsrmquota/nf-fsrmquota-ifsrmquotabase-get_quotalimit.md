---
UID: NF:fsrmquota.IFsrmQuotaBase.get_QuotaLimit
title: IFsrmQuotaBase::get_QuotaLimit
author: windows-sdk-content
description: Retrieves or sets the quota limit for the object.
old-location: fsrm\ifsrmquotabase_quotalimit.htm
old-project: Fsrm
ms.assetid: 2f2b5d8f-70b7-497e-9c51-171dca657c69
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmQuotaBase interface [File Server Resource Manager],QuotaLimit property, IFsrmQuotaBase.QuotaLimit, IFsrmQuotaBase.get_QuotaLimit, IFsrmQuotaBase::QuotaLimit, IFsrmQuotaBase::get_QuotaLimit, IFsrmQuotaBase::put_QuotaLimit, QuotaLimit property [File Server Resource Manager], QuotaLimit property [File Server Resource Manager],IFsrmQuotaBase interface, fs.ifsrmquotabase_quotalimit, fsrm.ifsrmquotabase_quotalimit, fsrmquota/IFsrmQuotaBase::QuotaLimit, fsrmquota/IFsrmQuotaBase::get_QuotaLimit, fsrmquota/IFsrmQuotaBase::put_QuotaLimit, get_QuotaLimit
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
 - IFsrmQuotaBase.QuotaLimit
 - IFsrmQuotaBase.get_QuotaLimit
 - IFsrmQuotaBase.put_QuotaLimit
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaBase::get_QuotaLimit


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves or sets the quota limit for the object.

This property is read/write.


## -parameters


## -remarks



If the quota limit is enforced, an IO operation that exceeds the limit will fail.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/88ff3968-cb83-4b66-83e9-a58205b4be82">Using Templates to Define Quotas</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7f4d5a73-a836-4ea1-bc53-d51433eeb02e">IFsrmQuotaBase</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

