---
UID: NF:mfobjects.IMFAttributes.GetItemType
title: IMFAttributes::GetItemType (mfobjects.h)
description: Retrieves the data type of the value associated with a key.
helpviewer_keywords: ["2c3a3c30-da10-4365-9f76-598a4ca7675c","GetItemType","GetItemType method [Media Foundation]","GetItemType method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetItemType method","IMFAttributes.GetItemType","IMFAttributes::GetItemType","mf.imfattributes_getitemtype","mfobjects/IMFAttributes::GetItemType"]
old-location: mf\imfattributes_getitemtype.htm
tech.root: mf
ms.assetid: 2c3a3c30-da10-4365-9f76-598a4ca7675c
ms.date: 12/05/2018
ms.keywords: 2c3a3c30-da10-4365-9f76-598a4ca7675c, GetItemType, GetItemType method [Media Foundation], GetItemType method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetItemType method, IMFAttributes.GetItemType, IMFAttributes::GetItemType, mf.imfattributes_getitemtype, mfobjects/IMFAttributes::GetItemType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAttributes::GetItemType
 - mfobjects/IMFAttributes::GetItemType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAttributes.GetItemType
---

# IMFAttributes::GetItemType


## -description

Retrieves the data type of the value associated with a key.

## -parameters

### -param guidKey [in]

GUID that identifies which value to query.

### -param pType [out]

Receives a member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a> enumeration.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key is not stored in this object.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>