---
UID: NN:shobjidl_core.IPersistFolder3
title: IPersistFolder3
author: windows-sdk-content
description: Extends the IPersistFolder and IPersistFolder2 interfaces by allowing a folder object to implement nondefault handling of folder shortcuts.
old-location: shell\IPersistFolder3.htm
old-project: shell
ms.assetid: 77a10997-1512-41ee-a84c-f3fa2e500d20
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IPersistFolder3, IPersistFolder3 interface [Windows Shell], IPersistFolder3 interface [Windows Shell],described, _win32_IPersistFolder3, shell.IPersistFolder3, shobjidl_core/IPersistFolder3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP3, Windows XP [desktop apps only]
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IPersistFolder3
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IPersistFolder3 interface


## -description


Extends the <a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a> and <a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a> interfaces by allowing a folder object to implement nondefault handling of folder shortcuts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistFolder3</b> interface inherits from <a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a>. <b>IPersistFolder3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistFolder3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97a343af-0998-4718-8293-1eb4d2ac0c8a">GetFolderTargetInfo</a>
</td>
<td align="left" width="63%">
Provides the location and attributes of a folder shortcut's target folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50a426b5-a526-4d3d-a20a-67050229f02e">InitializeEx</a>
</td>
<td align="left" width="63%">
Initializes a folder and specifies its location in the namespace. If the folder is a shortcut, this method also specifies the location of the target folder.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a>, <a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>, and <a href="https://msdn.microsoft.com/3deb3467-b6f2-49f9-ba24-fd2cca80f247">IPersistFolder2</a> interfaces, from which it inherits.

In Windows versions earlier than Windows Vista, this interface was declared in Shlobj.h.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Namespace extensions implement this interface if they need to perform nondefault handling of folder shortcuts.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications do not normally use this interface directly.



