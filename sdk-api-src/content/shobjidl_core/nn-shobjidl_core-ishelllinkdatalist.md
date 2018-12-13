---
UID: NN:shobjidl_core.IShellLinkDataList
title: IShellLinkDataList
author: windows-sdk-content
description: Exposes methods that allow an application to attach extra data blocks to a Shell link. These methods add, copy, or remove data blocks.
old-location: shell\IShellLinkDataList.htm
tech.root: shell
ms.assetid: ac3279ad-1413-48bf-a830-4ec128352573
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IShellLinkDataList, IShellLinkDataList interface [Windows Shell], IShellLinkDataList interface [Windows Shell],described, _win32_IShellLinkDataList, shell.IShellLinkDataList, shobjidl_core/IShellLinkDataList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLinkDataList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellLinkDataList interface


## -description


Exposes methods that allow an application to attach extra data blocks to a <a href="https://msdn.microsoft.com/32ad306d-54bd-4130-ad30-08db50ef106e">Shell link</a>. These methods add, copy, or remove data blocks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellLinkDataList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellLinkDataList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellLinkDataList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6580736f-e217-4e3e-9b6e-1c1c004916f4">AddDataBlock</a>
</td>
<td align="left" width="63%">
Adds a data block to a link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e02fb4c3-faec-40cc-ab97-d05cdcc148ed">CopyDataBlock</a>
</td>
<td align="left" width="63%">
Retrieves a copy of a link's data block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6ebfd84-6ef4-43be-af16-71fc395c4735">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the current option settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32660c95-4b09-4ede-b02d-bf3a335a9097">RemoveDataBlock</a>
</td>
<td align="left" width="63%">
Removes a data block from a link.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fca6394-e8ad-4ef3-a7d8-60e85229556b">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the current option settings.

</td>
</tr>
</table> 


## -remarks



The data blocks are in the form of a structure. The first two members are the same for all data blocks. The first member gives the structure's size. The second member is a signature that identifies the type of data block. The remaining members hold the block's data. There are five types of data block currently supported.
				


<table class="clsStd">
<tr>
<th>Data block structure</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb773274(v=VS.85).aspx">EXP_DARWIN_LINK</a>
</td>
<td>The link's Windows Installer ID.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb773279(v=VS.85).aspx">EXP_SPECIAL_FOLDER</a>
</td>
<td>Special folder information.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb773282(v=VS.85).aspx">EXP_SZ_LINK</a>
</td>
<td>The target name.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb773359(v=VS.85).aspx">NT_CONSOLE_PROPS</a>
</td>
<td>Console properties.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Bb773362(v=VS.85).aspx">NT_FE_CONSOLE_PROPS</a>
</td>
<td>The console's code page.</td>
</tr>
</table>
 



This interface is not implemented by applications.

Use this interface if your application needs to add extra data blocks to a Shell link.

<div class="alert"><b>Note</b>  <b>Windows Vista and later.</b> Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


