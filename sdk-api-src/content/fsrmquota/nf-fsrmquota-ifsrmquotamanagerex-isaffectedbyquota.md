---
UID: NF:fsrmquota.IFsrmQuotaManagerEx.IsAffectedByQuota
title: IFsrmQuotaManagerEx::IsAffectedByQuota
author: windows-sdk-content
description: Retrieves a value that determines whether a specified path is subject to a quota.
old-location: fsrm\ifsrmquotamanagerex_isaffectedbyquota.htm
old-project: Fsrm
ms.assetid: 8b366eae-5554-4c20-9ba9-c3a6e319712f
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IFsrmQuotaManagerEx interface [File Server Resource Manager],IsAffectedByQuota method, IFsrmQuotaManagerEx.IsAffectedByQuota, IFsrmQuotaManagerEx::IsAffectedByQuota, IsAffectedByQuota, IsAffectedByQuota method [File Server Resource Manager], IsAffectedByQuota method [File Server Resource Manager],IFsrmQuotaManagerEx interface, fs.ifsrmquotamanagerex_isaffectedbyquota, fsrm.ifsrmquotamanagerex_isaffectedbyquota, fsrmquota/IFsrmQuotaManagerEx::IsAffectedByQuota
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
 - IFsrmQuotaManagerEx.IsAffectedByQuota
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmQuotaManagerEx::IsAffectedByQuota


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a> class.]

Retrieves a value that determines whether a specified path is subject to a quota.


## -parameters




### -param path [in]

The local directory path to determine whether a quota applies.


### -param options [in]

The options to use when checking for a quota. For possible values, see the 
     <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param affected [out]

Is <b>VARIANT_TRUE</b> if the path referred to by the 
     <i>path</i> parameter is subject to a quota, otherwise it is 
     <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/aa665a9d-d053-49e4-82a7-d6ba27406a7c">IFsrmQuotaManagerEx</a>



<a href="https://msdn.microsoft.com/9308f1de-ba8e-45f5-81ec-d8203839ee79">MSFT_FSRMQuota</a>
 

 

