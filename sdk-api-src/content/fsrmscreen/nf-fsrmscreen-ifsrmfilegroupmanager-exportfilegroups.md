---
UID: NF:fsrmscreen.IFsrmFileGroupManager.ExportFileGroups
title: IFsrmFileGroupManager::ExportFileGroups method
author: windows-driver-content
description: Exports the specified file groups as an XML string.
old-location: fsrm\ifsrmfilegroupmanager_exportfilegroups.htm
old-project: Fsrm
ms.assetid: 59d7ef32-f06b-4167-8e28-da88da27ab0a
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: ExportFileGroups method [File Server Resource Manager], ExportFileGroups method [File Server Resource Manager], FsrmFileGroupManager class, ExportFileGroups method [File Server Resource Manager], IFsrmFileGroupManager interface, ExportFileGroups,IFsrmFileGroupManager.ExportFileGroups, FsrmFileGroupManager class [File Server Resource Manager], ExportFileGroups method, IFsrmFileGroupManager, IFsrmFileGroupManager interface [File Server Resource Manager], ExportFileGroups method, IFsrmFileGroupManager::ExportFileGroups, fs.ifsrmfilegroupmanager_exportfilegroups, fsrm.ifsrmfilegroupmanager_exportfilegroups, fsrmscreen/IFsrmFileGroupManager::ExportFileGroups
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileGroupManager.ExportFileGroups
-	FsrmFileGroupManager.ExportFileGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileGroupManager::ExportFileGroups method


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

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
    <a href="https://msdn.microsoft.com/81f62d49-5fce-4d8c-96b5-506d741c5f77">IFsrmFileGroupManager::ImportFileGroups</a> 
    method to import the file groups.




## -see-also




<a href="https://msdn.microsoft.com/d5c9c8f0-edbe-4f34-8f34-fe9d0667926e">FsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/e0a1a3d3-f683-410d-a0d9-081cd2476d1e">IFsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

