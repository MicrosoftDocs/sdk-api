---
UID: NF:fsrmquota.IFsrmAutoApplyQuota.get_ExcludeFolders
title: IFsrmAutoApplyQuota::get_ExcludeFolders
author: windows-sdk-content
description: Retrieves or sets an array of immediate subdirectories to exclude from the automatic quota.
old-location: fsrm\ifsrmautoapplyquota_excludefolders.htm
old-project: fsrm
ms.assetid: 1682e53c-f494-4fa4-b192-203b76e47394
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: ExcludeFolders property [File Server Resource Manager], ExcludeFolders property [File Server Resource Manager],IFsrmAutoApplyQuota interface, IFsrmAutoApplyQuota interface [File Server Resource Manager],ExcludeFolders property, IFsrmAutoApplyQuota.ExcludeFolders, IFsrmAutoApplyQuota.get_ExcludeFolders, IFsrmAutoApplyQuota::ExcludeFolders, IFsrmAutoApplyQuota::get_ExcludeFolders, IFsrmAutoApplyQuota::put_ExcludeFolders, fs.ifsrmautoapplyquota_excludefolders, fsrm.ifsrmautoapplyquota_excludefolders, fsrmquota/IFsrmAutoApplyQuota::ExcludeFolders, fsrmquota/IFsrmAutoApplyQuota::get_ExcludeFolders, fsrmquota/IFsrmAutoApplyQuota::put_ExcludeFolders, get_ExcludeFolders
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmquota.h
req.include-header: 
req.redist: 
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
 - IFsrmAutoApplyQuota.ExcludeFolders
 - IFsrmAutoApplyQuota.get_ExcludeFolders
 - IFsrmAutoApplyQuota.put_ExcludeFolders
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmAutoApplyQuota::get_ExcludeFolders


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a> class.]

Retrieves or sets an array of immediate subdirectories to exclude from the automatic 
    quota.

This property is read/write.


## -parameters


## -remarks



The list can contain the names of existing subdirectories or subdirectories that may exist in the future.

Setting this property overwrites the current list of subdirectories to exclude. To remove all folders, pass an 
    empty array.




## -see-also




<a href="https://msdn.microsoft.com/3eb30caa-ce29-4898-b1a7-bd905031ca98">IFsrmAutoApplyQuota</a>



<a href="https://msdn.microsoft.com/3941d07c-67e3-4763-8113-31fc156c9bd0">MSFT_FSRMAutoQuota</a>
 

 

