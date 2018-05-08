---
UID: NN:shldisp.FolderItems2
title: FolderItems2
author: windows-driver-content
description: Extends the FolderItems object. It supports one additional method.
old-location: shell\FolderItems2_Object.htm
old-project: shell
ms.assetid: 0ca0efb3-6831-4561-9fd1-6d0b62704931
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: FolderItems2, FolderItems2 object [Windows Shell], FolderItems2 object [Windows Shell],described, _win32_FolderItems2_Object, shell.FolderItems2_Object, shldisp/FolderItems2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	FolderItems2
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# FolderItems2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/b99201b3-95e8-4ddd-b338-dee8d107d0a0">FolderItems</a> object. It supports one additional method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">FolderItems2</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>FolderItems2</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c02985d-8877-4a02-a232-6aeb1716928c">InvokeVerbEx</a>
</td>
<td align="left" width="63%">
Executes a verb on a collection of <a href="https://msdn.microsoft.com/38c0e049-2f9f-43bc-8bf2-1b7becf16e66">FolderItem</a> objects. This method is an extension of the <a href="https://msdn.microsoft.com/569bdc88-15ef-4d08-923c-4f41e5ae5a38">InvokeVerb</a> method, allowing additional control of the operation through a set of flags.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a>



<a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>
 

 

