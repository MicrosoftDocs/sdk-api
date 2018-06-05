---
UID: NF:fsrmscreen.IFsrmFileGroupManager.EnumFileGroups
title: IFsrmFileGroupManager::EnumFileGroups
author: windows-sdk-content
description: Enumerates the file groups in FSRM.
old-location: fsrm\ifsrmfilegroupmanager_enumfilegroups.htm
old-project: Fsrm
ms.assetid: 317eb6cf-7bcc-4042-a7b7-05efac84a0c2
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: EnumFileGroups, EnumFileGroups method [File Server Resource Manager], EnumFileGroups method [File Server Resource Manager],FsrmFileGroupManager class, EnumFileGroups method [File Server Resource Manager],IFsrmFileGroupManager interface, FsrmFileGroupManager class [File Server Resource Manager],EnumFileGroups method, IFsrmFileGroupManager interface [File Server Resource Manager],EnumFileGroups method, IFsrmFileGroupManager.EnumFileGroups, IFsrmFileGroupManager::EnumFileGroups, fs.ifsrmfilegroupmanager_enumfilegroups, fsrm.ifsrmfilegroupmanager_enumfilegroups, fsrmscreen/IFsrmFileGroupManager::EnumFileGroups
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileGroupManager.EnumFileGroups
-	FsrmFileGroupManager.EnumFileGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileGroupManager::EnumFileGroups


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Enumerates the file groups in FSRM.


## -parameters




### -param options [in]

One or more options for enumerating the file groups. For possible values, see the 
      <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param fileGroups [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface 
       that contains a collection of file groups. Each item of the collection is a 
       <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the 
       <b>pdispVal</b> member of the variant for the 
       <a href="https://msdn.microsoft.com/9b657f1c-1d59-4ba5-9af9-978ffda1a348">IFsrmFileGroup</a> interface.

The collection contains only committed file groups; the collection will not contain newly created file groups 
       that have not been committed.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/d5c9c8f0-edbe-4f34-8f34-fe9d0667926e">FsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/e0a1a3d3-f683-410d-a0d9-081cd2476d1e">IFsrmFileGroupManager</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

