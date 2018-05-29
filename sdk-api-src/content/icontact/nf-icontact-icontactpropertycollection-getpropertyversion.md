---
UID: NF:icontact.IContactPropertyCollection.GetPropertyVersion
title: IContactPropertyCollection::GetPropertyVersion
author: windows-sdk-content
description: Retrieves the version number for the current property in the enumeration.
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyVersion.htm
old-project: wincontacts
ms.assetid: ff10129e-45cb-41a4-8800-22b33a238b65
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GetPropertyVersion, GetPropertyVersion method [Windows Contacts], GetPropertyVersion method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyVersion method, IContactPropertyCollection.GetPropertyVersion, IContactPropertyCollection::GetPropertyVersion, _wincontacts_IContactPropertyCollection_GetPropertyVersion, icontact/IContactPropertyCollection::GetPropertyVersion, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyVersion
ms.prod: windows
ms.technology: windows-sdk
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
-	IContactPropertyCollection.GetPropertyVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactPropertyCollection::GetPropertyVersion


## -description


Retrieves the version number for the current property in the enumeration.


## -parameters




### -param pdwVersion [in, out]

Type: <b>DWORD*</b>

Specifies the version of the property. 


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
 



