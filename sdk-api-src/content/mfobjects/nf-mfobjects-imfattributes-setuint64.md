---
UID: NF:mfobjects.IMFAttributes.SetUINT64
title: IMFAttributes::SetUINT64 (mfobjects.h)
description: Associates a UINT64 value with a key.
helpviewer_keywords: ["817ed1c1-16ad-4520-a1a0-a93563936b50","IMFAttributes interface [Media Foundation]","SetUINT64 method","IMFAttributes.SetUINT64","IMFAttributes::SetUINT64","SetUINT64","SetUINT64 method [Media Foundation]","SetUINT64 method [Media Foundation]","IMFAttributes interface","mf.imfattributes_setuint64","mfobjects/IMFAttributes::SetUINT64"]
old-location: mf\imfattributes_setuint64.htm
tech.root: mf
ms.assetid: 817ed1c1-16ad-4520-a1a0-a93563936b50
ms.date: 12/05/2018
ms.keywords: 817ed1c1-16ad-4520-a1a0-a93563936b50, IMFAttributes interface [Media Foundation],SetUINT64 method, IMFAttributes.SetUINT64, IMFAttributes::SetUINT64, SetUINT64, SetUINT64 method [Media Foundation], SetUINT64 method [Media Foundation],IMFAttributes interface, mf.imfattributes_setuint64, mfobjects/IMFAttributes::SetUINT64
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
 - IMFAttributes::SetUINT64
 - mfobjects/IMFAttributes::SetUINT64
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
 - IMFAttributes.SetUINT64
---

# IMFAttributes::SetUINT64


## -description

Associates a <b>UINT64</b> value with a key.

## -parameters

### -param guidKey [in]

GUID that identifies the value to set. If this key already exists, the method overwrites the old value.

### -param unValue [in]

New value for this key.

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

To retrieve the <b>UINT64</b> value, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>