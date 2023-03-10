---
UID: NF:mfobjects.IMFAttributes.GetCount
title: IMFAttributes::GetCount (mfobjects.h)
description: Retrieves the number of attributes that are set on this object.
helpviewer_keywords: ["5f511d5c-249c-4311-8380-a932a755eaaf","GetCount","GetCount method [Media Foundation]","GetCount method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetCount method","IMFAttributes.GetCount","IMFAttributes::GetCount","mf.imfattributes_getcount","mfobjects/IMFAttributes::GetCount"]
old-location: mf\imfattributes_getcount.htm
tech.root: mf
ms.assetid: 5f511d5c-249c-4311-8380-a932a755eaaf
ms.date: 12/05/2018
ms.keywords: 5f511d5c-249c-4311-8380-a932a755eaaf, GetCount, GetCount method [Media Foundation], GetCount method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetCount method, IMFAttributes.GetCount, IMFAttributes::GetCount, mf.imfattributes_getcount, mfobjects/IMFAttributes::GetCount
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
 - IMFAttributes::GetCount
 - mfobjects/IMFAttributes::GetCount
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
 - IMFAttributes.GetCount
---

# IMFAttributes::GetCount


## -description

Retrieves the number of attributes that are set on this object.

## -parameters

### -param pcItems [out]

Receives the number of attributes. This parameter must not be <b>NULL</b>. If this parameter is <b>NULL</b>, an access violation occurs.

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

To enumerate all of the attributes, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getitembyindex">IMFAttributes::GetItemByIndex</a> for each index value.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>