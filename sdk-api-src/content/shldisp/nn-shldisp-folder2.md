---
UID: NN:shldisp.Folder2
title: Folder2
author: windows-sdk-content
description: Extends the Folder object to support offline folders.
old-location: shell\Folder2_Object.htm
old-project: shell
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Folder2, Folder2 object [Windows Shell], Folder2 object [Windows Shell],described, _win32_Folder2_Object, shell.Folder2_Object, shldisp/Folder2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Folder2
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# Folder2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a> object to support offline folders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Folder2</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>Folder2</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/170893b6-c947-45b1-b717-a93a0b083bda">DismissedWebViewBarricade</a>
</td>
<td align="left" width="63%">
Called in response to the web view barricade being dismissed by the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f">Synchronize</a>
</td>
<td align="left" width="63%">
Synchronizes all offline files in the folder.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Folder2</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/28baaa6f-ae39-4110-b341-199ebda9d578">HaveToShowWebViewBarricade</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b50b130d-0675-49b5-b730-f67ea1c71d8c">OfflineStatus</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the offline status of the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0964505d-4138-4444-91d4-46c707c45688">Self</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains the folder's <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f1e82c61-205e-47c8-bc7c-6a52410a672e">Folder</a>
 

 

