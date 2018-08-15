---
UID: NF:fsrmscreen.IFsrmFileGroup.get_NonMembers
title: IFsrmFileGroup::get_NonMembers
author: windows-sdk-content
description: Retrieves or sets the filename patterns that determine the files that are excluded from the file group.
old-location: fsrm\ifsrmfilegroup_nonmembers.htm
old-project: fsrm
ms.assetid: c3c2ff78-db1a-44df-a7af-15c4a6c4b22d
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: IFsrmFileGroup interface [File Server Resource Manager],NonMembers property, IFsrmFileGroup.NonMembers, IFsrmFileGroup.get_NonMembers, IFsrmFileGroup::NonMembers, IFsrmFileGroup::get_NonMembers, IFsrmFileGroup::put_NonMembers, NonMembers property [File Server Resource Manager], NonMembers property [File Server Resource Manager],IFsrmFileGroup interface, fs.ifsrmfilegroup_nonmembers, fsrm.ifsrmfilegroup_nonmembers, fsrmscreen/IFsrmFileGroup::NonMembers, fsrmscreen/IFsrmFileGroup::get_NonMembers, fsrmscreen/IFsrmFileGroup::put_NonMembers, get_NonMembers
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
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
 - IFsrmFileGroup.NonMembers
 - IFsrmFileGroup.get_NonMembers
 - IFsrmFileGroup.put_NonMembers
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileGroup::get_NonMembers


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/c090da1e-df74-4dba-aaa0-15defa85d604">MSFT_FSRMFileGroup</a> class.]

Retrieves or sets the filename patterns that determine the files that are excluded from the file 
    group.

This property is read/write.


## -parameters


## -remarks



A filename pattern is a string expression that defines a set of filenames. The expression may contain the 
    following wildcard characters: "*" and "?". The "*" wildcard 
    matches 0 or more characters and the "?" wildcard  matches exactly 1 character. For example, the 
    file name "example.cpp" matches the pattern "e*.cpp", 
    but not "e?.cpp". The filename "ex.cpp" would match 
    both patterns. Note that when the filename pattern is used to compare against a specific filename, the pattern 
    match is case-insensitive.

You use the property to allow file patterns that would otherwise be blocked by the 
    <a href="https://msdn.microsoft.com/242a86ab-9dec-4106-9a49-70c12cc6de91">Members</a> property. For example, if 
    <b>Members</b> property uses 
    "*.mp*" to block mp3 files, you could set this property to 
    "*.mpp" to allow "*.mpp" files.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/951f5757-28fb-4583-9850-a11f60df05f5">Creating File Groups to Specify the Files to Restrict</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b657f1c-1d59-4ba5-9af9-978ffda1a348">IFsrmFileGroup</a>
 

 

