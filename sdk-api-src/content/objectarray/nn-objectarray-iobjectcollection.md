---
UID: NN:objectarray.IObjectCollection
title: IObjectCollection
author: windows-sdk-content
description: Extends the IObjectArray interface by providing methods that enable clients to add and remove objects that support IUnknown in a collection.
old-location: shell\IObjectCollection.htm
tech.root: shell
ms.assetid: d7665b26-5839-4b08-a099-ef25a68c65db
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IObjectCollection, IObjectCollection interface [Windows Shell], IObjectCollection interface [Windows Shell],described, _shell_IObjectCollection, objectarray/IObjectCollection, shell.IObjectCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objectarray.h
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
 - objectarray.h
api_name:
 - IObjectCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectCollection interface


## -description


Extends the <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> interface by providing methods that enable clients to add and remove objects that support <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> in a collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectCollection</b> interface inherits from <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>. <b>IObjectCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc51b2e0-a5e0-4440-a279-e94640b5dda7">AddFromArray</a>
</td>
<td align="left" width="63%">
Adds the objects contained in an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0898160d-46e5-4b38-9fc9-f74bd6a0385b">AddObject</a>
</td>
<td align="left" width="63%">
Adds a single object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b32ce885-aafe-4c81-8e7a-74f67fa15180">Clear</a>
</td>
<td align="left" width="63%">
Removes all objects from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0e526c0-a374-4952-8fe1-2a5aa53d9c41">RemoveObjectAt</a>
</td>
<td align="left" width="63%">
Removes a single, specified object from the collection.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to interact with a collection of generic objects.



