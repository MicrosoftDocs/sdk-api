---
UID: NN:shldisp.Folder
title: Folder
author: windows-sdk-content
description: Represents a Shell folder. This object contains properties and methods that allow you to retrieve information about the folder.
old-location: shell\Folder.htm
old-project: shell
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Folder, Folder object [Windows Shell], Folder object [Windows Shell],described, _win32_Folder, shell.Folder, shldisp/Folder
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
 - Shldisp.h
api_name:
 - Folder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder interface


## -description


Represents a Shell folder. This object contains properties and methods that allow you to retrieve information about the folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Folder</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>Folder</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22bf1b4c-f242-4c52-b094-c5339bb35d02">CopyHere</a>
</td>
<td align="left" width="63%">
Copies an item or items to a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2fe4550-f171-40d9-8bce-065b61826997">GetDetailsOf</a>
</td>
<td align="left" width="63%">
Retrieves details about an item in a folder. For example, its size, type, or the time of its last modification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef2965ec-c8ab-4108-8e5e-b4fd5370521a">Items</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object that represents the collection of items in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07723dc1-5d9d-4f32-ab18-52617b0988c4">MoveHere</a>
</td>
<td align="left" width="63%">
Moves an item or items to this folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87">NewFolder</a>
</td>
<td align="left" width="63%">
Creates a new folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a>
</td>
<td align="left" width="63%">
Creates and returns a <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object that represents a specified item.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Folder</b> object has these properties.
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
Contains the folder's Application object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/235106cc-ac49-4824-84ec-f7ea867cc028">Parent</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b832948c-f599-4ada-8760-9280b86abfed">ParentFolder</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the parent <b>Folder</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn923257">Title</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the title of the folder.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Not all methods are implemented for all folders. For example, the <a href="https://msdn.microsoft.com/3af7052c-fb81-4a96-9bf9-379b0365a376">ParseName</a> method is not implemented for the Control Panel folder (CSIDL_CONTROLS). If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</div>
<div> </div>


