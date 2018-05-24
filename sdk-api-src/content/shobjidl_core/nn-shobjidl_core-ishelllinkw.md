---
UID: NN:shobjidl_core.IShellLinkW
title: IShellLinkW
author: windows-driver-content
description: Exposes methods that create, modify, and resolve Shell links.
old-location: shell\IShellLink.htm
old-project: shell
ms.assetid: 67982d28-27ce-4482-b588-10fec8143750
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IShellLink, IShellLink interface [Windows Shell], IShellLink interface [Windows Shell],described, IShellLinkA, IShellLinkW, _win32_IShellLink, _win32_IShellLink_cpp, shell.IShellLink, shobjidl_core/IShellLink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellLink
-	IShellLinkW
-	IShellLinkA
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellLinkW interface


## -description


Exposes methods that create, modify, and resolve Shell links.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellLink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellLink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellLink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd807387-1998-4b38-996f-6dbacefffa48">GetArguments</a>
</td>
<td align="left" width="63%">
Gets the command-line arguments associated with a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546575">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the description string for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e3572bf-8d68-4485-99e8-bf47192be821">GetHotkey</a>
</td>
<td align="left" width="63%">
Gets the keyboard shortcut (hot key) for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff7cc9be-a762-472a-9846-4dbd0ec94ad1">GetIconLocation</a>
</td>
<td align="left" width="63%">
Gets the location (path and index) of the icon for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae1ac1b0-bcaf-4e3b-831c-f843ae86779c">GetIDList</a>
</td>
<td align="left" width="63%">
Gets the list of item identifiers for the target of a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a>
</td>
<td align="left" width="63%">
Gets the path and file name of the target of a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbd89c28-86e1-4a2c-b3ea-d934f263b59f">GetShowCmd</a>
</td>
<td align="left" width="63%">
Gets the show command for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cae6b2fd-362b-43a2-b0cb-b42bd103f359">GetWorkingDirectory</a>
</td>
<td align="left" width="63%">
Gets the name of the working directory for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a31f1d6d-7b87-4777-89a8-a032b7629b7e">Resolve</a>
</td>
<td align="left" width="63%">
Attempts to find the target of a Shell link, even if it has been moved or renamed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">SetArguments</a>
</td>
<td align="left" width="63%">
Sets the command-line arguments for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bec482e-04e6-4cde-ab8e-23c5a1463bdf">SetDescription</a>
</td>
<td align="left" width="63%">
Sets the description for a Shell link object. The description can be any application-defined string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82cc2af8-b872-4efc-bfe4-04a50df74e28">SetHotkey</a>
</td>
<td align="left" width="63%">
Sets a keyboard shortcut (hot key) for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ba267f2-ae05-4a6d-be3c-382a89e17d92">SetIconLocation</a>
</td>
<td align="left" width="63%">
Sets the location (path and index) of the icon for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c0571a5-1615-4c3f-b9a6-0667df07165b">SetIDList</a>
</td>
<td align="left" width="63%">
Sets the PIDL for a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/032610ba-d6ff-4200-8fd3-455460587dec">SetPath</a>
</td>
<td align="left" width="63%">
Sets the path and file name for the target of a Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">SetRelativePath</a>
</td>
<td align="left" width="63%">
Sets the relative path to the Shell link object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f40cd7d-04b5-4880-831f-5fb5cd52a2eb">SetShowCmd</a>
</td>
<td align="left" width="63%">
Sets the show command for a Shell link object. The show command sets the initial show state of the window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03767add-766c-4970-935e-ffa5aa401a95">SetWorkingDirectory</a>
</td>
<td align="left" width="63%">
Sets the name of the working directory for a Shell link object.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  This interface cannot be used to create a link to a URL.</div>
<div> </div>
The <b>IShellLink</b> interface has an ANSI version (<b>IShellLinkA</b>) and a Unicode version (<b>IShellLinkW</b>). The version that will be used depends on whether you compile for ANSI or Unicode.



