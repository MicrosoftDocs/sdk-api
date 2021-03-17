---
UID: NF:mfobjects.IMFAttributes.SetString
title: IMFAttributes::SetString (mfobjects.h)
description: Associates a wide-character string with a key.
helpviewer_keywords: ["51d2a2a0-92cb-49e0-b4a9-7201e9d92322","IMFAttributes interface [Media Foundation]","SetString method","IMFAttributes.SetString","IMFAttributes::SetString","SetString","SetString method [Media Foundation]","SetString method [Media Foundation]","IMFAttributes interface","mf.imfattributes_setstring","mfobjects/IMFAttributes::SetString"]
old-location: mf\imfattributes_setstring.htm
tech.root: mf
ms.assetid: 51d2a2a0-92cb-49e0-b4a9-7201e9d92322
ms.date: 12/05/2018
ms.keywords: 51d2a2a0-92cb-49e0-b4a9-7201e9d92322, IMFAttributes interface [Media Foundation],SetString method, IMFAttributes.SetString, IMFAttributes::SetString, SetString, SetString method [Media Foundation], SetString method [Media Foundation],IMFAttributes interface, mf.imfattributes_setstring, mfobjects/IMFAttributes::SetString
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
 - IMFAttributes::SetString
 - mfobjects/IMFAttributes::SetString
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
 - IMFAttributes.SetString
---

# IMFAttributes::SetString


## -description

Associates a wide-character string with a key.

## -parameters

### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.

### -param wszValue [in]

Null-terminated wide-character string to associate with this key. The method stores a copy of the string.

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
</table>

## -remarks

To retrieve the string, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring">IMFAttributes::GetString</a> or <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring">IMFAttributes::GetAllocatedString</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>