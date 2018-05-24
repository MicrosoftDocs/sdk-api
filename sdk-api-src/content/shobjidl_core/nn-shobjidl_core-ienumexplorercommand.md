---
UID: NN:shobjidl_core.IEnumExplorerCommand
title: IEnumExplorerCommand
author: windows-driver-content
description: Provided by an IExplorerCommandProvider. This interface contains the enumeration of commands to be put into the command bar.
old-location: shell\IEnumExplorerCommand.htm
old-project: shell
ms.assetid: c9a21e84-dd95-413a-b9db-e02008185bef
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IEnumExplorerCommand, IEnumExplorerCommand interface [Windows Shell], IEnumExplorerCommand interface [Windows Shell],described, _shell_IEnumExplorerCommand, shell.IEnumExplorerCommand, shobjidl_core/IEnumExplorerCommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	shobjidl_core.h
api_name:
-	IEnumExplorerCommand
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IEnumExplorerCommand interface


## -description


Provided by an <a href="https://msdn.microsoft.com/f39ea1f7-28ba-4a5e-ac19-bcfc6052fdeb">IExplorerCommandProvider</a>. This interface contains the enumeration of commands to be put into the command bar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumExplorerCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumExplorerCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumExplorerCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of elements that directly follow the current element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
</table> 


## -remarks



None of the methods of this interface should talk to network resources. They are called on the UI thread; communicating with network resources would cause the UI to stop responding.



