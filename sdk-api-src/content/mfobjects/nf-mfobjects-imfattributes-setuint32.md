---
UID: NF:mfobjects.IMFAttributes.SetUINT32
title: IMFAttributes::SetUINT32 (mfobjects.h)
description: Associates a UINT32 value with a key.
helpviewer_keywords: ["9c30fd56-719f-4831-8fbf-cefcf9d72709","IMFAttributes interface [Media Foundation]","SetUINT32 method","IMFAttributes.SetUINT32","IMFAttributes::SetUINT32","SetUINT32","SetUINT32 method [Media Foundation]","SetUINT32 method [Media Foundation]","IMFAttributes interface","mf.imfattributes_setuint32","mfobjects/IMFAttributes::SetUINT32"]
old-location: mf\imfattributes_setuint32.htm
tech.root: mf
ms.assetid: 9c30fd56-719f-4831-8fbf-cefcf9d72709
ms.date: 12/05/2018
ms.keywords: 9c30fd56-719f-4831-8fbf-cefcf9d72709, IMFAttributes interface [Media Foundation],SetUINT32 method, IMFAttributes.SetUINT32, IMFAttributes::SetUINT32, SetUINT32, SetUINT32 method [Media Foundation], SetUINT32 method [Media Foundation],IMFAttributes interface, mf.imfattributes_setuint32, mfobjects/IMFAttributes::SetUINT32
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
 - IMFAttributes::SetUINT32
 - mfobjects/IMFAttributes::SetUINT32
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
 - IMFAttributes.SetUINT32
---

# IMFAttributes::SetUINT32


## -description

Associates a <b>UINT32</b> value with a key.

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

To retrieve the <b>UINT32</b> value, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32">IMFAttributes::GetUINT32</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>