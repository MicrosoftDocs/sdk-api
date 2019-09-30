---
UID: NN:fsrmscreen.IFsrmFileScreen
title: IFsrmFileScreen (fsrmscreen.h)
author: windows-sdk-content
description: Used to configure a file screen that blocks groups of files from being saved to the specified directory.
old-location: fsrm\ifsrmfilescreen.htm
tech.root: fsrm
ms.assetid: 69b831a1-c935-4de0-b222-009bafc45ec5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmFileScreen, IFsrmFileScreen interface [File Server Resource Manager], IFsrmFileScreen interface [File Server Resource Manager],described, fs.ifsrmfilescreen, fsrm.ifsrmfilescreen, fsrmscreen/IFsrmFileScreen
ms.topic: interface
f1_keywords: 
 - "fsrmscreen/IFsrmFileScreen"
req.header: fsrmscreen.h
req.include-header: 
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
 - IFsrmFileScreen
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileScreen interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a> class.]

Used to configure a file screen that blocks groups of files from being saved to the specified 
    directory.

To create this interface, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-createfilescreen">IFsrmFileScreenManager::CreateFileScreen</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-enumfilescreens">IFsrmFileScreenManager::EnumFileScreens</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenmanager-getfilescreen">IFsrmFileScreenManager::GetFileScreen</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreen</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>. <b>IFsrmFileScreen</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmFileScreen</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-applytemplate">ApplyTemplate</a>
</td>
<td align="left" width="63%">
Applies the property values of the specified file screen template to this file screen object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreen</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-get_matchessourcetemplate">MatchesSourceTemplate</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves a value that determines whether the property values of this file screen object match those values 
     of the template from which the object was derived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-get_path">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the path of the directory to which the file screen object applies.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-get_sourcetemplatename">SourceTemplateName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the name of the template from which this file screen object was derived.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-get_useraccount">UserAccount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The account name of the user whose files will be screened

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreen-get_usersid">UserSid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The SID of the user whose files will be screened

</td>
</tr>
</table> 


## -remarks



A file screen limits the types of files that the system or any user can store in a directory. When a 
    restricted file is detected, the FSRM server performs the specified actions (see 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreenbase-createaction">IFsrmFileScreenBase::CreateAction</a>).

The file screen applies to future files—the screen is not applied retroactively. To list 
    the files in the directory that violate the screen, create a report job that lists files by type.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenbase">IFsrmFileScreenBase</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenexception">IFsrmFileScreenException</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/msft-fsrmfilescreen">MSFT_FSRMFileScreen</a>
 

 

