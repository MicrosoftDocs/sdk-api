---
UID: NF:fsrmquota.IFsrmAutoApplyQuota.put_ExcludeFolders
title: IFsrmAutoApplyQuota::put_ExcludeFolders (fsrmquota.h)
description: Retrieves or sets an array of immediate subdirectories to exclude from the automatic quota. (Put)
helpviewer_keywords: ["ExcludeFolders property [File Server Resource Manager]","ExcludeFolders property [File Server Resource Manager]","IFsrmAutoApplyQuota interface","IFsrmAutoApplyQuota interface [File Server Resource Manager]","ExcludeFolders property","IFsrmAutoApplyQuota.ExcludeFolders","IFsrmAutoApplyQuota.put_ExcludeFolders","IFsrmAutoApplyQuota::ExcludeFolders","IFsrmAutoApplyQuota::get_ExcludeFolders","IFsrmAutoApplyQuota::put_ExcludeFolders","fs.ifsrmautoapplyquota_excludefolders","fsrm.ifsrmautoapplyquota_excludefolders","fsrmquota/IFsrmAutoApplyQuota::ExcludeFolders","fsrmquota/IFsrmAutoApplyQuota::get_ExcludeFolders","fsrmquota/IFsrmAutoApplyQuota::put_ExcludeFolders","put_ExcludeFolders"]
old-location: fsrm\ifsrmautoapplyquota_excludefolders.htm
tech.root: fsrm
ms.assetid: 1682e53c-f494-4fa4-b192-203b76e47394
ms.date: 12/05/2018
ms.keywords: ExcludeFolders property [File Server Resource Manager], ExcludeFolders property [File Server Resource Manager],IFsrmAutoApplyQuota interface, IFsrmAutoApplyQuota interface [File Server Resource Manager],ExcludeFolders property, IFsrmAutoApplyQuota.ExcludeFolders, IFsrmAutoApplyQuota.put_ExcludeFolders, IFsrmAutoApplyQuota::ExcludeFolders, IFsrmAutoApplyQuota::get_ExcludeFolders, IFsrmAutoApplyQuota::put_ExcludeFolders, fs.ifsrmautoapplyquota_excludefolders, fsrm.ifsrmautoapplyquota_excludefolders, fsrmquota/IFsrmAutoApplyQuota::ExcludeFolders, fsrmquota/IFsrmAutoApplyQuota::get_ExcludeFolders, fsrmquota/IFsrmAutoApplyQuota::put_ExcludeFolders, put_ExcludeFolders
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmAutoApplyQuota::put_ExcludeFolders
 - fsrmquota/IFsrmAutoApplyQuota::put_ExcludeFolders
dev_langs:
 - c++
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
---

# IFsrmAutoApplyQuota::put_ExcludeFolders


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a> class.]

Retrieves or sets an array of immediate subdirectories to exclude from the automatic 
    quota.

This property is read/write.

## -parameters

## -remarks

The list can contain the names of existing subdirectories or subdirectories that may exist in the future.

Setting this property overwrites the current list of subdirectories to exclude. To remove all folders, pass an 
    empty array.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmautoapplyquota">IFsrmAutoApplyQuota</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmautoquota">MSFT_FSRMAutoQuota</a>
