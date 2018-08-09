---
UID: NN:fsrmscreen.IFsrmFileGroup
title: IFsrmFileGroup
author: windows-sdk-content
description: Used to define a group of files based on one or more file name patterns.
old-location: fsrm\ifsrmfilegroup.htm
old-project: fsrm
ms.assetid: 9b657f1c-1d59-4ba5-9af9-978ffda1a348
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmFileGroup, IFsrmFileGroup interface [File Server Resource Manager], IFsrmFileGroup interface [File Server Resource Manager],described, fs.ifsrmfilegroup, fsrm.ifsrmfilegroup, fsrm/IFsrmFileGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: fsrmscreen.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
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
 - IFsrmFileGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileGroup interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Used to define a group of files based on one or more file name patterns. A file group is a 
    logical collection of file name patterns identified by name that is used to define file screens and file screen 
    exceptions. File group definitions may also be used for generating storage report jobs based on file type.

To create a file group, call the 
    <a href="https://msdn.microsoft.com/7e2c3672-fbb9-4da5-9e20-25c66213843c">IFsrmFileGroupManager::CreateFileGroup</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/317eb6cf-7bcc-4042-a7b7-05efac84a0c2">IFsrmFileGroupManager::EnumFileGroups</a>
</li>
<li>
<a href="https://msdn.microsoft.com/14b61b2b-a20e-4895-bfbe-40e9dfe0c496">IFsrmFileGroupManager::GetFileGroup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/81f62d49-5fce-4d8c-96b5-506d741c5f77">IFsrmFileGroupManager::ImportFileGroups</a>
</li>
</ul>

## -remarks



A file group is formed by including all members and then excluding all nonmembers. For example, to list all 
    files except for <i>examplename</i>, set <b>Members</b> 
    to "*.*" and <b>NonMembers</b> to 
    "<i>examplename</i>".




## -see-also




<a href="https://msdn.microsoft.com/bbd888d9-1005-4173-8e82-ced13e68c09e">FSRM Interfaces</a>



<a href="https://msdn.microsoft.com/bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7">IFsrmObject</a>



<a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a>
 

 

