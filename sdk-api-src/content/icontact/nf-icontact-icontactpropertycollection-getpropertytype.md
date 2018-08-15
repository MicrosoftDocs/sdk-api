---
UID: NF:icontact.IContactPropertyCollection.GetPropertyType
title: IContactPropertyCollection::GetPropertyType
author: windows-sdk-content
description: Retrieves the type for the current property in the enumeration.
old-location: wincontacts\_wincontacts_IContactPropertyCollection_GetPropertyType.htm
old-project: wincontacts
ms.assetid: 11977b0c-332a-415a-986f-7fb08246413f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CGD_ARRAY_NODE, CGD_BINARY_PROPERTY, CGD_DATE_PROPERTY, CGD_STRING_PROPERTY, CGD_UNKNOWN_PROPERTY, GetPropertyType, GetPropertyType method [Windows Contacts], GetPropertyType method [Windows Contacts],IContactPropertyCollection interface, IContactPropertyCollection interface [Windows Contacts],GetPropertyType method, IContactPropertyCollection.GetPropertyType, IContactPropertyCollection::GetPropertyType, _wincontacts_IContactPropertyCollection_GetPropertyType, icontact/IContactPropertyCollection::GetPropertyType, wincontacts._wincontacts_IContactPropertyCollection_GetPropertyType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: icontact.h
req.include-header: Contact.h
req.redist: 
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
tech.root: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wab32.dll
api_name:
 - IContactPropertyCollection.GetPropertyType
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactPropertyCollection::GetPropertyType


## -description


Retrieves the type for the current property in the enumeration.


## -parameters




### -param pdwType [in, out]

Type: <b>DWORD*</b>

Specifies the type of property. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CGD_UNKNOWN_PROPERTY"></a><a id="cgd_unknown_property"></a><dl>
<dt><b>CGD_UNKNOWN_PROPERTY</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CGD_STRING_PROPERTY"></a><a id="cgd_string_property"></a><dl>
<dt><b>CGD_STRING_PROPERTY</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CGD_DATE_PROPERTY"></a><a id="cgd_date_property"></a><dl>
<dt><b>CGD_DATE_PROPERTY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CGD_BINARY_PROPERTY"></a><a id="cgd_binary_property"></a><dl>
<dt><b>CGD_BINARY_PROPERTY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CGD_ARRAY_NODE"></a><a id="cgd_array_node"></a><dl>
<dt><b>CGD_ARRAY_NODE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 


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
 



