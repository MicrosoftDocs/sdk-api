---
UID: NN:shlobj_core.IShellDetails
title: IShellDetails
author: windows-sdk-content
description: Exposed by Shell folders to provide detailed information about the items in a folder.
old-location: shell\IShellDetails.htm
tech.root: shell
ms.assetid: c31409fd-9350-46bb-a8a0-85d5958c6e49
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IShellDetails, IShellDetails interface [Windows Shell], IShellDetails interface [Windows Shell],described, _win32_IShellDetails, shell.IShellDetails, shlobj_core/IShellDetails
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDetails
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellDetails interface


## -description


Exposed by Shell folders to provide detailed information about the items in a folder. This is the same information that is displayed by the Windows Explorer when the view of the folder is set to Details. For Windows 2000 and later systems, <b>IShellDetails</b> is superseded by <a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDetails</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellDetails</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellDetails</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df37b2c7-16ea-4768-a1c2-6ccec4fecde9">ColumnClick</a>
</td>
<td align="left" width="63%">
Rearranges a column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5442dc80-9ecf-4e47-a84d-6da4327696ef">GetDetailsOf</a>
</td>
<td align="left" width="63%">
Gets detailed information on an item in a Shell folder.

</td>
</tr>
</table> 


## -remarks



For Windows 2000 and later systems, folder objects should implement <a href="https://msdn.microsoft.com/9b008034-3576-429e-b67c-e2222592ca46">IShellFolder2</a> instead of this interface. However, if your application needs to function on earlier systems, <b>IShellDetails</b> should also be exposed.



