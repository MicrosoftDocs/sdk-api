---
UID: NN:unknwn.IClassFactory
title: IClassFactory
author: windows-sdk-content
description: Enables a class of objects to be created.
old-location: com\iclassfactory.htm
old-project: com
ms.assetid: f624f833-2b69-43bc-92cd-c4ecbe6051c5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IClassFactory, IClassFactory interface [COM], IClassFactory interface [COM],described, _com_iclassfactory, com.iclassfactory, unknwnbase/IClassFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: unknwn.h
req.include-header: Unknwn.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - unknwnbase.h
api_name:
 - IClassFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IClassFactory interface


## -description


Enables a class of objects to be created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IClassFactory</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IClassFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IClassFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45d34150-9e0b-4a76-a784-c81434ec73b8">CreateInstance</a>
</td>
<td align="left" width="63%">
Creates an uninitialized object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c817b89-013d-477f-a713-5e320896dfa0">LockServer</a>
</td>
<td align="left" width="63%">
Locks an object application open in memory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/65e758ce-50a4-49e8-b3b2-0cd148d2781a">CoGetClassObject</a>



<a href="https://msdn.microsoft.com/00b7edd2-8e2e-4e0a-91a6-d966f6c8d456">OleCreate</a>
 

 

