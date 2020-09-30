---
UID: NF:mfobjects.IMFAttributes.CompareItem
title: IMFAttributes::CompareItem (mfobjects.h)
description: Queries whether a stored attribute value equals to a specified PROPVARIANT.
helpviewer_keywords: ["CompareItem","CompareItem method [Media Foundation]","CompareItem method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","CompareItem method","IMFAttributes.CompareItem","IMFAttributes::CompareItem","f0a6073b-fce6-4a1f-b7d1-ef6543e7648f","mf.imfattributes_compareitem","mfobjects/IMFAttributes::CompareItem"]
old-location: mf\imfattributes_compareitem.htm
tech.root: mf
ms.assetid: f0a6073b-fce6-4a1f-b7d1-ef6543e7648f
ms.date: 12/05/2018
ms.keywords: CompareItem, CompareItem method [Media Foundation], CompareItem method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],CompareItem method, IMFAttributes.CompareItem, IMFAttributes::CompareItem, f0a6073b-fce6-4a1f-b7d1-ef6543e7648f, mf.imfattributes_compareitem, mfobjects/IMFAttributes::CompareItem
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
 - IMFAttributes::CompareItem
 - mfobjects/IMFAttributes::CompareItem
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
 - IMFAttributes.CompareItem
---

# IMFAttributes::CompareItem


## -description

Queries whether a stored attribute value equals to a specified <b>PROPVARIANT</b>.

## -parameters

### -param guidKey [in]

GUID that identifies which value to query.

### -param Value [in]

<b>PROPVARIANT</b> that contains the value to compare.

### -param pbResult [out]

Receives a Boolean value indicating whether the attribute matches the value given in <i>Value</i>. See Remarks. This parameter must not be <b>NULL</b>. If this parameter is <b>NULL</b>, an access violation occurs.

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

The method sets <i>pbResult</i> to <b>FALSE</b> for any of the following reasons:

<ul>
<li>
No attribute is found whose key matches the one given in <i>guidKey</i>.

</li>
<li>
The attribute's <b>PROPVARIANT</b> type does not match the type given in <i>Value</i>.

</li>
<li>
The attribute value does not match the value given in <i>Value</i>.

</li>
<li>
The method fails.

</li>
</ul>
Otherwise, the method sets <i>pbResult</i> to <b>TRUE</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>