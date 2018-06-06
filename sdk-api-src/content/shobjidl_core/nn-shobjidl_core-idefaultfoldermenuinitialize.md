---
UID: NN:shobjidl_core.IDefaultFolderMenuInitialize
title: IDefaultFolderMenuInitialize
author: windows-sdk-content
description: Provides methods used to get and set shortcut menu information. This information is the same as that provided to SHCreateDefaultContextMenu through the DEFCONTEXTMENU structure.
old-location: shell\IDefaultFolderMenuInitialize.htm
old-project: shell
ms.assetid: 23C75435-E43D-4451-8F03-AE051BC1B66D
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDefaultFolderMenuInitialize, IDefaultFolderMenuInitialize interface [Windows Shell], IDefaultFolderMenuInitialize interface [Windows Shell],described, shell.IDefaultFolderMenuInitialize, shobjidl_core/IDefaultFolderMenuInitialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - IDefaultFolderMenuInitialize
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IDefaultFolderMenuInitialize interface


## -description


Provides methods used to get and set shortcut menu information. This information is the same as that provided to <a href="https://msdn.microsoft.com/055ff0a0-9ba7-463d-9684-3fd072b190da">SHCreateDefaultContextMenu</a> through the <a href="https://msdn.microsoft.com/007861f6-1e66-4c5f-a459-3cfbe9f8cec2">DEFCONTEXTMENU</a> structure.
<div class="alert"><b>Note</b>  Do not use this method to reinitialize a shortcut menu; use <a href="https://msdn.microsoft.com/1997a32e-562a-4d20-ad09-c40446a8feed">IShellExtInit::Initialize</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultFolderMenuInitialize</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDefaultFolderMenuInitialize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDefaultFolderMenuInitialize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/373240B8-E99E-4ff9-B47A-3B31B4F0B81E">GetMenuRestrictions</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90D861DA-33B7-4054-888E-86B504B2C5D1">SetHandlerClsid</a>
</td>
<td align="left" width="63%"></td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7D907B01-E0C4-428b-A8A4-FA383B0970BF">SetMenuRestrictions</a>
</td>
<td align="left" width="63%"></td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

