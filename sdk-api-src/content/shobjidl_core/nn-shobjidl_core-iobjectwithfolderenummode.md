---
UID: NN:shobjidl_core.IObjectWithFolderEnumMode
title: IObjectWithFolderEnumMode
author: windows-sdk-content
description: Exposes methods that get and set enumeration modes of a parsed item.
old-location: shell\IObjectWithFolderEnumMode.htm
tech.root: shell
ms.assetid: 33838ddc-8e0e-431a-a957-40e23f0ad0c7
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IObjectWithFolderEnumMode, IObjectWithFolderEnumMode interface [Windows Shell], IObjectWithFolderEnumMode interface [Windows Shell],described, _shell_IObjectWithFolderEnumMode, shell.IObjectWithFolderEnumMode, shobjidl_core/IObjectWithFolderEnumMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IObjectWithFolderEnumMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectWithFolderEnumMode interface


## -description


Exposes methods that get and set enumeration modes of a parsed item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithFolderEnumMode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithFolderEnumMode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithFolderEnumMode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d331255-2295-4f7b-b2d6-1238edcc15bb">GetMode</a>
</td>
<td align="left" width="63%">
Retrieves the enumeration mode of the parsed item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e7271ec-47a7-42bf-ab02-26cd587448bd">SetMode</a>
</td>
<td align="left" width="63%">
Sets the enumeration mode of the parsed item.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented as part of a Shell namespace extension, specifically the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
This interface is used by the <a href="https://msdn.microsoft.com/099e71b0-04f2-4f82-aa00-7581bd357900">IShellFolder::ParseDisplayName</a> method to retrieve the <a href="https://msdn.microsoft.com/ef360e40-63c9-49a0-bcfa-1f2e2ff11a3a">FOLDER_ENUM_MODE</a> value which controls the enumeration mode of the parsed item.

Items with different enumeration modes compare canonically different (SHCIDS_CANONICALONLY) because they enumerate different sets of items.



