---
UID: NN:shobjidl_core.IPersistFolder2
title: IPersistFolder2
author: windows-sdk-content
description: Exposes methods that obtain information from Shell folder objects.
old-location: shell\IPersistFolder2.htm
old-project: shell
ms.assetid: 3deb3467-b6f2-49f9-ba24-fd2cca80f247
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPersistFolder2, IPersistFolder2 interface [Windows Shell], IPersistFolder2 interface [Windows Shell],described, _win32_IPersistFolder2, shell.IPersistFolder2, shobjidl_core/IPersistFolder2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
-	IPersistFolder2
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IPersistFolder2 interface


## -description


Exposes methods that obtain information from Shell folder objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistFolder2</b> interface inherits from <a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a>. <b>IPersistFolder2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistFolder2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aaf6ed5-ae8e-4521-80cb-ec45af8827aa">GetCurFolder</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> for the folder object.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/932eb0e2-35a6-482e-9138-00cff30508a9">IPersist</a>, <a href="https://msdn.microsoft.com/d37d4ca5-93a0-4090-b657-9b23d5df875c">IPersistFolder</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
When implementing a Shell namespace extension, specifically the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface, you need to implement this interface so that the Shell folder object's <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> can be retrieved.



