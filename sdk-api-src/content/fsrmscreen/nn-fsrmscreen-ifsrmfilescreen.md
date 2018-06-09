---
UID: NN:fsrmscreen.IFsrmFileScreen
title: IFsrmFileScreen
author: windows-sdk-content
description: Used to configure a file screen that blocks groups of files from being saved to the specified directory.
old-location: fsrm\ifsrmfilescreen.htm
old-project: Fsrm
ms.assetid: 69b831a1-c935-4de0-b222-009bafc45ec5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IFsrmFileScreen, IFsrmFileScreen interface [File Server Resource Manager], IFsrmFileScreen interface [File Server Resource Manager],described, fs.ifsrmfilescreen, fsrm.ifsrmfilescreen, fsrmscreen/IFsrmFileScreen
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IFsrmFileScreen
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreen interface


## -description


<p class="CCE_Message">[This interface is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a> class.]

Used to configure a file screen that blocks groups of files from being saved to the specified 
    directory.

To create this interface, call the 
    <a href="https://msdn.microsoft.com/5e35c647-2b5a-486b-b8c5-0bc25bd313ad">IFsrmFileScreenManager::CreateFileScreen</a> 
    method.

The following methods return this interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/5826d5c3-885a-4001-aa89-0bc1c03b9338">IFsrmFileScreenManager::EnumFileScreens</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9af0d9a7-80a2-4cc8-a703-c1af8ac5b7c9">IFsrmFileScreenManager::GetFileScreen</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmFileScreen</b> interface inherits from <a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>. <b>IFsrmFileScreen</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d495cb92-09c4-4fa5-873c-5f07475eb7bf">ApplyTemplate</a>
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

<a href="https://msdn.microsoft.com/9ea79d7e-2f81-46c4-8afe-ebe4e2f3c49f">MatchesSourceTemplate</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915708">Path</a>


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

<a href="https://msdn.microsoft.com/12dffc6e-77d0-4010-ae7c-94a4be2549e6">SourceTemplateName</a>


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

<a href="https://msdn.microsoft.com/c47a61b8-3e9b-404f-9100-8e8ccb08ecd1">UserAccount</a>


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

<a href="https://msdn.microsoft.com/7f5c549d-52a3-4013-9f86-844d823636f6">UserSid</a>


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
    <a href="https://msdn.microsoft.com/1d627e07-fa8c-4c22-acba-c08767b8ebaa">IFsrmFileScreenBase::CreateAction</a>).

The file screen applies to future files—the screen is not applied retroactively. To list 
    the files in the directory that violate the screen, create a report job that lists files by type.




## -see-also




<a href="https://msdn.microsoft.com/9e52af8c-e03b-4b44-83bd-541fe1419d6c">IFsrmFileScreenBase</a>



<a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a>



<a href="https://msdn.microsoft.com/86ee74e0-64d5-478a-8150-0f4b37e56694">MSFT_FSRMFileScreen</a>
 

 

