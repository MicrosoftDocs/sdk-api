---
UID: NF:fsrmscreen.IFsrmFileGroupManager.ExportFileGroups
title: IFsrmFileGroupManager::ExportFileGroups (fsrmscreen.h)
description: Exports the specified file groups as an XML string.
helpviewer_keywords: ["ExportFileGroups","ExportFileGroups method [File Server Resource Manager]","ExportFileGroups method [File Server Resource Manager]","FsrmFileGroupManager class","ExportFileGroups method [File Server Resource Manager]","IFsrmFileGroupManager interface","FsrmFileGroupManager class [File Server Resource Manager]","ExportFileGroups method","IFsrmFileGroupManager interface [File Server Resource Manager]","ExportFileGroups method","IFsrmFileGroupManager.ExportFileGroups","IFsrmFileGroupManager::ExportFileGroups","fs.ifsrmfilegroupmanager_exportfilegroups","fsrm.ifsrmfilegroupmanager_exportfilegroups","fsrmscreen/IFsrmFileGroupManager::ExportFileGroups"]
old-location: fsrm\ifsrmfilegroupmanager_exportfilegroups.htm
tech.root: fsrm
ms.assetid: 59d7ef32-f06b-4167-8e28-da88da27ab0a
ms.date: 12/05/2018
ms.keywords: ExportFileGroups, ExportFileGroups method [File Server Resource Manager], ExportFileGroups method [File Server Resource Manager],FsrmFileGroupManager class, ExportFileGroups method [File Server Resource Manager],IFsrmFileGroupManager interface, FsrmFileGroupManager class [File Server Resource Manager],ExportFileGroups method, IFsrmFileGroupManager interface [File Server Resource Manager],ExportFileGroups method, IFsrmFileGroupManager.ExportFileGroups, IFsrmFileGroupManager::ExportFileGroups, fs.ifsrmfilegroupmanager_exportfilegroups, fsrm.ifsrmfilegroupmanager_exportfilegroups, fsrmscreen/IFsrmFileGroupManager::ExportFileGroups
req.header: fsrmscreen.h
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
 - IFsrmFileGroupManager::ExportFileGroups
 - fsrmscreen/IFsrmFileGroupManager::ExportFileGroups
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
 - IFsrmFileGroupManager.ExportFileGroups
 - FsrmFileGroupManager.ExportFileGroups
---

# IFsrmFileGroupManager::ExportFileGroups


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Exports the specified file groups as an XML string.

## -parameters

### -param fileGroupNamesArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of the names 
      of the file groups to export. If <b>NULL</b>, the method exports all file groups.

### -param serializedFileGroups [out]

The specified file groups in XML format.

## -returns

The method returns the following return values.

## -remarks

Typically, you use this method to save the file groups information to a file. You can then copy the file to 
    another computer and call the 
    <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-importfilegroups">IFsrmFileGroupManager::ImportFileGroups</a> 
    method to import the file groups.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilegroupmanager">FsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroupmanager">IFsrmFileGroupManager</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>