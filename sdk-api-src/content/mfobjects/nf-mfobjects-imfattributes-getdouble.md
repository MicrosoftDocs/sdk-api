---
UID: NF:mfobjects.IMFAttributes.GetDouble
title: IMFAttributes::GetDouble (mfobjects.h)
description: Retrieves a double value associated with a key.
helpviewer_keywords: ["650a5f7f-609f-477b-8834-ff66ca3a9ca3","GetDouble","GetDouble method [Media Foundation]","GetDouble method [Media Foundation]","IMFAttributes interface","IMFActivate.GetDouble","IMFAttributes interface [Media Foundation]","GetDouble method","IMFAttributes.GetDouble","IMFAttributes::GetDouble","mf.imfattributes_getdouble","mfobjects/IMFAttributes::GetDouble"]
old-location: mf\imfattributes_getdouble.htm
tech.root: mf
ms.assetid: 650a5f7f-609f-477b-8834-ff66ca3a9ca3
ms.date: 12/05/2018
ms.keywords: 650a5f7f-609f-477b-8834-ff66ca3a9ca3, GetDouble, GetDouble method [Media Foundation], GetDouble method [Media Foundation],IMFAttributes interface, IMFActivate.GetDouble, IMFAttributes interface [Media Foundation],GetDouble method, IMFAttributes.GetDouble, IMFAttributes::GetDouble, mf.imfattributes_getdouble, mfobjects/IMFAttributes::GetDouble
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
 - IMFAttributes::GetDouble
 - mfobjects/IMFAttributes::GetDouble
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
 - IMFAttributes.GetDouble
 - IMFActivate.GetDouble
---

# IMFAttributes::GetDouble


## -description

Retrieves a <b>double</b> value associated with a key.

## -parameters

### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_DOUBLE</b>.

### -param pfValue [out]

Receives a <b>double</b> value. If the key is found and the data type is <b>double</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.

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
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a <b>double</b>.

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



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributedouble">MFGetAttributeDouble</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>