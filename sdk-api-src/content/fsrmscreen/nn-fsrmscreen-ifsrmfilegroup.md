---
UID: NN:fsrmscreen.IFsrmFileGroup
title: IFsrmFileGroup (fsrmscreen.h)
author: windows-sdk-content
description: Used to define a group of files based on one or more file name patterns.
old-location: fsrm\ifsrmfilegroup.htm
tech.root: fsrm
ms.assetid: 9b657f1c-1d59-4ba5-9af9-978ffda1a348
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileGroup, IFsrmFileGroup interface [File Server Resource Manager], IFsrmFileGroup interface [File Server Resource Manager],described, fs.ifsrmfilegroup, fsrm.ifsrmfilegroup, fsrm/IFsrmFileGroup
ms.topic: interface
f1_keywords: ["fsrmscreen/IFsrmFileGroup"]
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
 - IFsrmFileGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileGroup interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Used to define a group of files based on one or more file name patterns. A file group is a 
    logical collection of file name patterns identified by name that is used to define file screens and file screen 
    exceptions. File group definitions may also be used for generating storage report jobs based on file type.

To create a file group, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-createfilegroup">IFsrmFileGroupManager::CreateFileGroup</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-enumfilegroups">IFsrmFileGroupManager::EnumFileGroups</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-getfilegroup">IFsrmFileGroupManager::GetFileGroup</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilegroupmanager-importfilegroups">IFsrmFileGroupManager::ImportFileGroups</a>
</li>
</ul>

## -remarks



A file group is formed by including all members and then excluding all nonmembers. For example, to list all 
    files except for <i>examplename</i>, set <b>Members</b> 
    to "*.*" and <b>NonMembers</b> to 
    "<i>examplename</i>".




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-interfaces">FSRM Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>
 

 

