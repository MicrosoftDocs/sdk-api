---
UID: NN:sdoias.ISdo
title: ISdo
author: windows-driver-content
description: Use the ISdo interface to store, retrieve, and update Server Data Objects (SDO) information.
old-location: nps\SDO_isdo.htm
old-project: Nps
ms.assetid: f8f49bf2-d8cc-40ad-ac52-05d74bcd931c
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ISdo, ISdo interface [Network Policy Server], ISdo interface [Network Policy Server],described, _sdo_isdo, nps.SDO_isdo, sdo.isdo, sdoias/ISdo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VENDORPROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Iassdo.dll
api_name:
-	ISdo
product: Windows
targetos: Windows
req.lib: 
req.dll: Iassdo.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISdo interface


## -description


Use the 
<b>ISdo</b> interface to store, retrieve, and update Server Data Objects (SDO) information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdo</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ISdo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aceca2f9-7b17-46a5-bcd1-e6fec3c369ed">Apply</a>
</td>
<td align="left" width="63%">
Writes changes to the datastore for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23033dc3-824c-429c-836d-65782ca3df92">get_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration interface for the object's properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9567e731-4240-4b37-8757-2e25824bba0a">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa2f0209-ec78-4b59-8f01-f1534b8894c1">GetPropertyInfo</a>
</td>
<td align="left" width="63%">
Retrieves an information interface for the specified property.

<b>Unsupported Interface:  </b>The <b>ISdoPropertyInfo</b> interface is unsupported and the use of this method to access it is discouraged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2e440a7-d58c-4542-bd0b-a06b810edd34">PutProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/650df0aa-6331-4a3f-b965-d48fd68fd31d">ResetProperty</a>
</td>
<td align="left" width="63%">
Resets the specified property to its default value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/446b1234-9b65-45dc-bb67-c315c26205dc">Restore</a>
</td>
<td align="left" width="63%">
Restores the values of the object's properties from the datastore.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/c7b8c59d-91a2-4dfd-a119-ecfd08dcd7aa">Server Data
    Objects Interfaces</a>



<a href="https://msdn.microsoft.com/0a73adfb-3f4b-46f6-8b76-d48f8599e05d">Server Data
    Objects Reference</a>
 

 

