---
UID: NF:mfobjects.IMFAttributes.GetUINT64
title: IMFAttributes::GetUINT64 (mfobjects.h)
description: Retrieves a UINT64 value associated with a key.
helpviewer_keywords: ["GetUINT64","GetUINT64 method [Media Foundation]","GetUINT64 method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetUINT64 method","IMFAttributes.GetUINT64","IMFAttributes::GetUINT64","f3240fff-48d8-4d88-8c75-15f00bfe72ed","mf.imfattributes_getuint64","mfobjects/IMFAttributes::GetUINT64"]
old-location: mf\imfattributes_getuint64.htm
tech.root: mf
ms.assetid: f3240fff-48d8-4d88-8c75-15f00bfe72ed
ms.date: 12/05/2018
ms.keywords: GetUINT64, GetUINT64 method [Media Foundation], GetUINT64 method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetUINT64 method, IMFAttributes.GetUINT64, IMFAttributes::GetUINT64, f3240fff-48d8-4d88-8c75-15f00bfe72ed, mf.imfattributes_getuint64, mfobjects/IMFAttributes::GetUINT64
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
 - IMFAttributes::GetUINT64
 - mfobjects/IMFAttributes::GetUINT64
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
 - IMFAttributes.GetUINT64
---

# IMFAttributes::GetUINT64


## -description

Retrieves a <b>UINT64</b> value associated with a key.

## -parameters

### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT64</b>.

### -param punValue [out]

Receives a <b>UINT64</b> value. If the key is found and the data type is <b>UINT64</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.

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
The attribute value is not a <b>UINT64</b>.
              

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



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeuint64">MFGetAttributeUINT64</a>



<a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>