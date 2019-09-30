---
UID: NN:fsrmscreen.IFsrmFileScreenBase
title: IFsrmFileScreenBase (fsrmscreen.h)
author: windows-sdk-content
description: Base class for all file screen interfaces.
old-location: fsrm\ifsrmfilescreenbase.htm
tech.root: fsrm
ms.assetid: 9e52af8c-e03b-4b44-83bd-541fe1419d6c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreenBase, IFsrmFileScreenBase interface [File Server Resource Manager], IFsrmFileScreenBase interface [File Server Resource Manager],described, fs.ifsrmfilescreenbase, fsrm.ifsrmfilescreenbase, fsrmscreen/IFsrmFileScreenBase
ms.topic: interface
f1_keywords: 
 - "fsrmscreen/IFsrmFileScreenBase"
req.header: fsrmscreen.h
req.include-header: FsrmScreen.h, FsrmTlb.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FsrmScreen.idl
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
 - IFsrmFileScreenBase
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileScreenBase interface


## -description


Base class for all file screen interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenBase</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>. <b>IFsrmFileScreenBase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileScreenBase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">CreateAction</a>
</td>
<td align="left" width="63%">
Creates an action for this file screen object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-enumactions">EnumActions</a>
</td>
<td align="left" width="63%">
Enumerates all the actions for the file screen object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreenBase</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-get_blockedfilegroups">BlockedFileGroups</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the names of the file groups that contain the file name patterns used to specify the files 
     that are blocked by this screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-get_filescreenflags">FileScreenFlags</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the file screen flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb625567(v=vs.85)">UserAccount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the string form of the user account that is associated with the file screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb625568(v=vs.85)">UserSid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the string form of the user's security identifier (SID) that is associated with the file 
     screen.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmobject">IFsrmObject</a>
 

 

