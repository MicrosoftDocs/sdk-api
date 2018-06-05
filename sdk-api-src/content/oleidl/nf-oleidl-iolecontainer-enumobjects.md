---
UID: NF:oleidl.IOleContainer.EnumObjects
title: IOleContainer::EnumObjects
author: windows-sdk-content
description: Enumerates the objects in the current container.
old-location: com\iolecontainer_enumobjects.htm
old-project: com
ms.assetid: 7d825c71-506c-4fd3-ab48-6006f2858d05
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EnumObjects, EnumObjects method [COM], EnumObjects method [COM],IOleContainer interface, IOleContainer interface [COM],EnumObjects method, IOleContainer.EnumObjects, IOleContainer::EnumObjects, _ole_iolecontainer_enumobjects, com.iolecontainer_enumobjects, oleidl/IOleContainer::EnumObjects
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OleIdl.h
api_name:
-	IOleContainer.EnumObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOleContainer::EnumObjects


## -description


Enumerates the objects in the current container.


## -parameters




### -param grfFlags [in]

Specifies which objects in a container are to be enumerated, as defined in the enumeration <a href="https://msdn.microsoft.com/9c70fc86-7166-47dd-a424-741f18e381e3">OLECONTF</a>.


### -param ppenum [out]

A pointer to an <a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a> pointer variable that receives the interface pointer to the enumerator object. Each time a container receives a successful call to <b>EnumObjects</b>, it must increase the reference count on the <i>ppenum</i> pointer the method returns. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when it is done with the pointer. If an error is returned, the implementation must set <i>ppenum</i> to <b>NULL</b>.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The operation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Object enumeration not supported.

</td>
</tr>
</table>
 




## -remarks



A container should implement <b>EnumObjects</b> to enable programmatic clients to find out what objects it holds. This method, however, is not called in standard linking scenarios.




## -see-also




<a href="https://msdn.microsoft.com/5aaed96f-39c1-4201-80d0-a2a8a177b65e">IEnumUnknown</a>



<a href="https://msdn.microsoft.com/98549309-8ac8-4391-92ab-8a62269ff579">IOleContainer</a>



<a href="https://msdn.microsoft.com/fe306a36-da24-4b1e-ab42-359d37962d36">IOleItemContainer</a>



<a href="https://msdn.microsoft.com/9c70fc86-7166-47dd-a424-741f18e381e3">OLECONTF</a>
 

 

