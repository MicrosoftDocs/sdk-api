---
UID: NN:iads.IADsCollection
title: IADsCollection
author: windows-sdk-content
description: The IADsCollection interface is a dual interface that enables its hosting ADSI object to define and manage an arbitrary set of named data elements for a directory service.
old-location: adsi\iadscollection.htm
old-project: ADSI
ms.assetid: 4552552b-c008-439a-95bf-eaf9ffd28b5f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsCollection, IADsCollection interface [ADSI], IADsCollection interface [ADSI],described, _ds_iadscollection, adsi.iadscollection, iads/IADsCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsCollection interface


## -description


The <b>IADsCollection</b> interface is a dual interface that enables its hosting ADSI object to define and manage an arbitrary set of named data elements for a directory service. Collections differ from arrays of elements in that individual items can be added or deleted without reordering the entire array.

Collection objects can represent one or more items that correspond to volatile data, such as processes or active communication sessions, as well as persistent data, such as physical entities for a directory service. For example, a collection object can represent a list of print jobs in a queue or a list of active sessions connected to a server. Although a collection object can represent arbitrary data sets, all elements in a collection must be of the same type. The data are of <b>Variant</b> types.

ADSI also exposes the  <a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a> and  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interfaces for manipulating two special cases of collection objects. <b>IADsMembers</b> is used for a collection of objects that share a common membership. An example of such objects are users that belong to a group. <b>IADsContainer</b> applies to an ADSI object that contains other objects. An example of this is a directory tree or a network topology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db2630d0-26be-4cf1-811e-fc1d2007dda5">get__NewEnum</a>
</td>
<td align="left" width="63%">
Gets an interface on an enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04b33451-505e-43de-8db4-3e37f9909ea6">GetObject</a>
</td>
<td align="left" width="63%">
Gets the specified item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an object from the collection.

</td>
</tr>
</table> 


## -remarks



Of the ADSI system providers, only the WinNT provider supports this interface to handle active file service sessions, resources and print jobs.




## -see-also




<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/889e8fc1-61a6-4a3a-82ac-85d41f664149">IADsMembers</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

