---
UID: NN:mfobjects.IMFCollection
title: IMFCollection
author: windows-sdk-content
description: Represents a generic collection of IUnknown pointers.
old-location: mf\imfcollection.htm
tech.root: medfound
ms.assetid: fec6aa17-2770-4f53-b36d-b94236093d23
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFCollection, IMFCollection interface [Media Foundation], IMFCollection interface [Media Foundation],described, fec6aa17-2770-4f53-b36d-b94236093d23, mf.imfcollection, mfobjects/IMFCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCollection interface


## -description


Represents a generic collection of <b>IUnknown</b> pointers.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ef2463b-3d5e-4ed0-ab7c-68758e6cc056">AddElement</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a45983a8-4061-40e1-a11a-67de0867e553">GetElement</a>
</td>
<td align="left" width="63%">
Retrieves an object in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bd46f66-0542-4185-b50e-163cc3b4e2f8">GetElementCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8f64bf8-eb5b-4673-91be-796f4ea8dce0">InsertElementAt</a>
</td>
<td align="left" width="63%">
Adds an object at the specified index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c82d287-b73e-46dd-a319-70c5d0f536c6">RemoveAllElements</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47f33235-6bb5-4103-82b4-87210b0e695c">RemoveElement</a>
</td>
<td align="left" width="63%">
Removes an object from the collection.

</td>
</tr>
</table> 


## -remarks



To create an empty collection object, call <a href="https://msdn.microsoft.com/6a7bf7b6-62f1-4eac-9849-39021ee50f42">MFCreateCollection</a>.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

