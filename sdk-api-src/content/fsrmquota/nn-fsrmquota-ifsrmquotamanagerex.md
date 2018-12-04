---
UID: NN:fsrmquota.IFsrmQuotaManagerEx
title: IFsrmQuotaManagerEx
author: windows-sdk-content
description: Used to manage quotas, extended version.
old-location: fsrm\ifsrmquotamanagerex.htm
tech.root: fsrm
ms.assetid: aa665a9d-d053-49e4-82a7-d6ba27406a7c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IFsrmQuotaManagerEx, IFsrmQuotaManagerEx interface [File Server Resource Manager], IFsrmQuotaManagerEx interface [File Server Resource Manager],described, fs.ifsrmquotamanagerex, fsrm.ifsrmquotamanagerex, fsrm/IFsrmQuotaManagerEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: fsrmquota.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmQuotaManagerEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmQuotaManagerEx interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Used to manage quotas, extended version.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmQuotaManagerEx</b> interface inherits from <a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>. <b>IFsrmQuotaManagerEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFsrmQuotaManagerEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b366eae-5554-4c20-9ba9-c3a6e319712f">IsAffectedByQuota</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether a specified path is subject to a quota.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/20bda7d6-5c7b-4066-82e2-83ad52515568">IFsrmQuotaManager</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

