---
UID: NN:shobjidl_core.IObjectWithProgID
title: IObjectWithProgID
author: windows-sdk-content
description: Exposes methods that provide access to the ProgID associated with an object.
old-location: shell\IObjectWithProgID.htm
old-project: shell
ms.assetid: 3b66ba49-ed39-464e-b15a-c72fdff7f5e5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IObjectWithProgID, IObjectWithProgID interface [Windows Shell], IObjectWithProgID interface [Windows Shell],described, _shell_IObjectWithProgID, shell.IObjectWithProgID, shobjidl_core/IObjectWithProgID
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
 - IObjectWithProgID
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IObjectWithProgID interface


## -description


Exposes methods that provide access to the ProgID associated with an object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectWithProgID</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectWithProgID</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectWithProgID</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37023615-09cb-4607-9496-7fe9d9f7c947">GetProgID</a>
</td>
<td align="left" width="63%">
Retrieves the ProgID associated with an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4889f9a5-da80-4909-b4b5-4ea69ea99c3e">SetProgID</a>
</td>
<td align="left" width="63%">
Sets the ProgID of an object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f2b666d6-bf22-47b5-87e1-8de5ff51c152">Programmatic Identifiers</a>
 

 

