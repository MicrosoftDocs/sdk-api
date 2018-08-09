---
UID: NN:iads.IADsDeleteOps
title: IADsDeleteOps
author: windows-sdk-content
description: The IADsDeleteOps interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.
old-location: adsi\iadsdeleteops.htm
old-project: ADSI
ms.assetid: 329d7061-9aa2-4f4e-a0ec-a0cbb1d231f5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsDeleteOps, IADsDeleteOps interface [ADSI], IADsDeleteOps interface [ADSI],described, _ds_iadsdeleteops, adsi.iadsdeleteops, iads/IADsDeleteOps
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsDeleteOps
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsDeleteOps interface


## -description


The <b>IADsDeleteOps</b> interface specifies a method an object can use to delete itself from the underlying directory. For a container object, the method deletes its children and the entire subtree.

The interface is designed to offer features that complement  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>. To remove an object from the directory store, request its parent object to perform the operation. That amounts to calling the  <a href="https://msdn.microsoft.com/2f3873e0-376e-4212-a28d-bd9bc112f6cf">IADsContainer::Delete</a> method on the contained object. When the object also implements the <b>IADsDeleteOps</b> interface, you can instruct the object to remove itself, and all the contained objects, by calling the <a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">IADsDeleteOps::DeleteObject</a> method directly on the object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsDeleteOps</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsDeleteOps</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsDeleteOps</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53685f60-9adf-40f0-b6d3-e59a0435f744">DeleteObject</a>
</td>
<td align="left" width="63%">
Deletes the object from the directory.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/87027c25-e3c9-4bad-8df3-cb6205e40ef6">Access Control and Object Deletion</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/2f3873e0-376e-4212-a28d-bd9bc112f6cf">IADsContainer::Delete</a>



<a href="https://msdn.microsoft.com/821b71c2-e9f5-4ca8-9366-e8a3f1907670">IADsDeleteOps Interface</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

