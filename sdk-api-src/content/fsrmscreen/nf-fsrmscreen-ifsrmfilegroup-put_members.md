---
UID: NF:fsrmscreen.IFsrmFileGroup.put_Members
title: IFsrmFileGroup::put_Members (fsrmscreen.h)
author: windows-sdk-content
description: Retrieves or sets the filename patterns that determine the files that are included in the file group.
old-location: fsrm\ifsrmfilegroup_members.htm
tech.root: fsrm
ms.assetid: 242a86ab-9dec-4106-9a49-70c12cc6de91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileGroup interface [File Server Resource Manager],Members property, IFsrmFileGroup.Members, IFsrmFileGroup.put_Members, IFsrmFileGroup::Members, IFsrmFileGroup::get_Members, IFsrmFileGroup::put_Members, Members property [File Server Resource Manager], Members property [File Server Resource Manager],IFsrmFileGroup interface, fs.ifsrmfilegroup_members, fsrm.ifsrmfilegroup_members, fsrmscreen/IFsrmFileGroup::Members, fsrmscreen/IFsrmFileGroup::get_Members, fsrmscreen/IFsrmFileGroup::put_Members, put_Members
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
 - IFsrmFileGroup.Members
 - IFsrmFileGroup.get_Members
 - IFsrmFileGroup.put_Members
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileGroup::put_Members


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a> class.]

Retrieves or sets the filename patterns that determine the files that are included in the file 
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


#### Examples

For an example, see 
      <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/creating-file-groups-to-specify-the-files-to-restrict">Creating File Groups to Specify the Files to Restrict</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilegroup">IFsrmFileGroup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilegroup">MSFT_FSRMFileGroup</a>
 

 

