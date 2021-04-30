---
UID: NF:mfobjects.IMFAttributes.Compare
title: IMFAttributes::Compare (mfobjects.h)
description: Compares the attributes on this object with the attributes on another object.
helpviewer_keywords: ["1d0c9d1c-448d-4851-b183-94b04acb2ab5","Compare","Compare method [Media Foundation]","Compare method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","Compare method","IMFAttributes.Compare","IMFAttributes::Compare","mf.imfattributes_compare","mfobjects/IMFAttributes::Compare"]
old-location: mf\imfattributes_compare.htm
tech.root: mf
ms.assetid: 1d0c9d1c-448d-4851-b183-94b04acb2ab5
ms.date: 12/05/2018
ms.keywords: 1d0c9d1c-448d-4851-b183-94b04acb2ab5, Compare, Compare method [Media Foundation], Compare method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],Compare method, IMFAttributes.Compare, IMFAttributes::Compare, mf.imfattributes_compare, mfobjects/IMFAttributes::Compare
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
 - IMFAttributes::Compare
 - mfobjects/IMFAttributes::Compare
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
 - IMFAttributes.Compare
---

# IMFAttributes::Compare


## -description

Compares the attributes on this object with the attributes on another object.

## -parameters

### -param pTheirs [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the object to compare with this object.

### -param MatchType [in]

Member of the <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attributes_match_type">MF_ATTRIBUTES_MATCH_TYPE</a> enumeration, specifying the type of comparison to make.

### -param pbResult [out]

Receives a Boolean value. The value is <b>TRUE</b> if the two sets of attributes match in the way specified by the <i>MatchType</i> parameter. Otherwise, the value is <b>FALSE</b>.

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

If <i>pThis</i> is the object whose <b>Compare</b> method is called, and <i>pTheirs</i> is the object passed in as the <i>pTheirs</i> parameter, the following comparisons are defined by <i>MatchType</i>.

<table>
<tr>
<th>Match type</th>
<th>Returns <b>TRUE</b> if and only if</th>
</tr>
<tr>
<td><b>MF_ATTRIBUTES_MATCH_OUR_ITEMS</b></td>
<td>For every attribute in <i>pThis</i>, an attribute with the same key and value exists in <i>pTheirs</i>.</td>
</tr>
<tr>
<td><b>MF_ATTRIBUTES_MATCH_THEIR_ITEMS</b></td>
<td>For every attribute in <i>pTheirs</i>, an attribute with the same key and value exists in <i>pThis</i>.</td>
</tr>
<tr>
<td><b>MF_ATTRIBUTES_MATCH_ALL_ITEMS</b></td>
<td>The key/value pairs are identical in both objects.</td>
</tr>
<tr>
<td><b>MF_ATTRIBUTES_MATCH_INTERSECTION</b></td>
<td>Take the intersection of the keys in <i>pThis</i> and the keys in <i>pTheirs</i>. The values associated with those keys are identical in both <i>pThis</i> and <i>pTheirs</i>.</td>
</tr>
<tr>
<td><b>MF_ATTRIBUTES_MATCH_SMALLER</b></td>
<td>Take the object with the smallest number of attributes. For every attribute in that object, an attribute with the same key and value exists in the other object.</td>
</tr>
</table>
 

The <i>pTheirs</i> and <i>pbResult</i> parameters must not be <b>NULL</b>. If either parameter is <b>NULL</b>, an access violation occurs.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>