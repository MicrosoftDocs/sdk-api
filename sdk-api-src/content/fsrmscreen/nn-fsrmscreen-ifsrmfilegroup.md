---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

