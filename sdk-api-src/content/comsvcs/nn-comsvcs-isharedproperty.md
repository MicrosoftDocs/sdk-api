---
UID: NN:comsvcs.ISharedProperty
title: ISharedProperty
author: windows-sdk-content
description: Exposes property methods that you can use to set or retrieve the value of a shared property.
old-location: cos\isharedproperty.htm
old-project: cossdk
ms.assetid: d3c3e888-fe08-4ea6-b94c-fdfcbe7fd08a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISharedProperty, ISharedProperty interface [COM+], ISharedProperty interface [COM+],described, _cos_ISharedProperty_Interface, comsvcs/ISharedProperty, cos.isharedproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISharedProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISharedProperty interface


## -description


Exposes property methods that you can use to set or retrieve the value of a shared property. A shared property can contain any data type that can be represented by a <b>Variant</b>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISharedProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b8e297c-db65-41b2-a5ee-3a63a4ff31fb">get_Value</a>
</td>
<td align="left" width="63%">
Retrieves the value of a shared property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d193990c-a804-41aa-81d7-75aced274f73">put_Value</a>
</td>
<td align="left" width="63%">
Sets the value of a shared property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e7f23c83-40d3-4b08-a185-cd6e3260e0a9">ISharedPropertyGroup</a>



<a href="https://msdn.microsoft.com/71c0a1de-5ea5-4496-b0e9-56d0cc8129a9">ISharedPropertyGroupManager</a>
 

 

