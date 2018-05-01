---
UID: NF:icontact.IContactPropertyCollection.GetPropertyModificationDate
title: IContactPropertyCollection::GetPropertyModificationDate method
author: windows-driver-content
description: Retrieves the last modification date for the current property in the enumeration. If not modified, contact creation date is returned.
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyModificationDate.htm
old-project: wincontacts
ms.assetid: 7ad95916-4e21-4607-b27d-584a931f9201
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetPropertyModificationDate method [Windows Contacts], GetPropertyModificationDate method [Windows Contacts], IContactPropertyCollection interface, GetPropertyModificationDate,IContactPropertyCollection.GetPropertyModificationDate, IContactPropertyCollection, IContactPropertyCollection interface [Windows Contacts], GetPropertyModificationDate method, IContactPropertyCollection::GetPropertyModificationDate, _wincontacts_IContactPropertyCollection_GetPropertyModificationDate, icontact/IContactPropertyCollection::GetPropertyModificationDate, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyModificationDate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: icontact.h
req.include-header: Contact.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wab32.dll
api_name:
-	IContactPropertyCollection.GetPropertyModificationDate
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactPropertyCollection::GetPropertyModificationDate method


## -description


Retrieves the last modification date for the current property in the enumeration. 
		If not modified, contact creation date is returned.


## -parameters




### -param pftModificationDate [in, out]

Type: <b><a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a>*</b>

Specifies the last modified date as a UTC FILETIME. 


## -returns



Type: <b>HRESULT</b>

Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Query is successful. 

</td>
</tr>
</table>
 



