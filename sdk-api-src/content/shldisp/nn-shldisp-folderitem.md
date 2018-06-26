---
UID: NN:shldisp.FolderItem
title: FolderItem
author: windows-sdk-content
description: Represents an item in a Shell folder. This object contains properties and methods that allow you to retrieve information about the item.
old-location: shell\FolderItem.htm
old-project: shell
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: FolderItem, FolderItem object [Windows Shell], FolderItem object [Windows Shell],described, _win32_FolderItem, shell.FolderItem, shldisp/FolderItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - FolderItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItem interface


## -description


Represents an item in a Shell folder. This object contains properties and methods that allow you to retrieve information about the item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">FolderItem</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>FolderItem</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/569bdc88-15ef-4d08-923c-4f41e5ae5a38">InvokeVerb</a>
</td>
<td align="left" width="63%">
Executes a verb on the item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e31160cd-093a-45a6-a066-58120c44eb2c">Verbs</a>
</td>
<td align="left" width="63%">
Retrieves the item's <a href="https://msdn.microsoft.com/31badb4b-b89e-4294-9dd7-bda716e163b2">FolderItemVerbs</a> object. This object is the collection of verbs that can be executed on the item.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">FolderItem</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/jj159071">Application</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the <a href="https://msdn.microsoft.com/library/windows/hardware/jj159071">Application</a> object of the folder item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/87afd0b6-245b-4550-9f21-aa0426ba8470">GetFolder</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the item's <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object, if the item is a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6444476a-a065-4f69-9330-584e30dbe30d">GetLink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the item's <a href="https://msdn.microsoft.com/d3c0ccf8-0f83-42f7-9d6f-1fb293da6364">ShellLinkObject</a> object, if the item is a shortcut.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/472e0906-9561-4390-a503-c5e490245ea0">IsBrowsable</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates if the item can be hosted inside a browser or Windows Explorer frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/321a2109-88b5-4a41-9a67-dab3e82e95d8">IsFileSystem</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates if the item is part of the file system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fb080c8f-04b1-4f9a-9219-0951a2e950ea">IsFolder</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates if the item is a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f3400f0b-5c7f-4d41-a162-1c35014082ac">IsLink</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the item is a shortcut.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bb60c800-863b-469b-b937-9816b8b338bf">ModifyDate</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the date and time that a file was last modified. <a href="https://msdn.microsoft.com/bb60c800-863b-469b-b937-9816b8b338bf">ModifyDate</a> can be used to retrieve the date and time that a folder was last modified, but cannot set it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Sets or gets the item's name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/612e76d8-d8bc-419c-b319-75b1f324840a">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an object that represents the parent of the item.

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
Contains the item's full path and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the item's size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains a string representation of the item's type.

</td>
</tr>
</table> 

