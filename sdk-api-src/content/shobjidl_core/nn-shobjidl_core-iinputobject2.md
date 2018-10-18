---
UID: NN:shobjidl_core.IInputObject2
title: IInputObject2
author: windows-sdk-content
description: Exposes a method that extends IInputObject by handling global accelerators.
old-location: shell\IInputObject2.htm
tech.root: shell
ms.assetid: 76d8672c-ea19-4d61-b6b5-e6c3951ec710
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IInputObject2, IInputObject2 interface [Windows Shell], IInputObject2 interface [Windows Shell],described, _shell_IInputObject2, shell.IInputObject2, shobjidl_core/IInputObject2
ms.prod: windows
ms.technology: windows-sdk
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
 - IInputObject2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInputObject2 interface


## -description


Exposes a method that extends <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a> by handling global accelerators.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputObject2</b> interface inherits from <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a>. <b>IInputObject2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputObject2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f55f2671-7164-421e-9269-aa70e85180de">TranslateAcceleratorGlobal</a>
</td>
<td align="left" width="63%">
Handles global accelerators so that input objects can respond to the keyboard even when they are not active in the UI.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/5fbbcd26-c60a-4b6a-92cf-36b8bd429266">IInputObject</a> interface, from which it inherits.



