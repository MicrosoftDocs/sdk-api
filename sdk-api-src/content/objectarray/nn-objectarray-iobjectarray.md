---
UID: NN:objectarray.IObjectArray
title: IObjectArray (objectarray.h)
author: windows-sdk-content
description: Exposes methods that enable clients to access items in a collection of objects that support IUnknown.
old-location: shell\IObjectArray.htm
tech.root: shell
ms.assetid: ab0bb213-dc9c-4853-98d7-668e7ca76583
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjectArray, IObjectArray interface [Windows Shell], IObjectArray interface [Windows Shell],described, _shell_IObjectArray, objectarray/IObjectArray, shell.IObjectArray
ms.topic: interface
f1_keywords: ["objectarray/IObjectArray"]
req.header: objectarray.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objectarray.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IObjectArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectArray interface


## -description


Exposes methods that enable clients to access items in a collection of objects that support <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectArray</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectArray</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IObjectArray</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objectarray/nf-objectarray-iobjectarray-getat">GetAt</a>
</td>
<td align="left" width="63%">
Provides a pointer to a specified object's interface. The object and interface are specified by index and interface ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/objectarray/nf-objectarray-iobjectarray-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Provides a count of the objects in the collection.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Clients do not need to implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to access generic objects in an array.



