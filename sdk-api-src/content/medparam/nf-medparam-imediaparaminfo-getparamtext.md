---
UID: NF:medparam.IMediaParamInfo.GetParamText
title: IMediaParamInfo::GetParamText (medparam.h)
description: The GetParamText method retrieves a series of text strings that describe the parameter.
helpviewer_keywords: ["GetParamText","GetParamText method [DirectShow]","GetParamText method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetParamText method","IMediaParamInfo.GetParamText","IMediaParamInfo::GetParamText","IMediaParamInfoGetParamText","dshow.imediaparaminfo_getparamtext","medparam/IMediaParamInfo::GetParamText"]
old-location: dshow\imediaparaminfo_getparamtext.htm
tech.root: dshow
ms.assetid: 38ecde61-fd4a-4ba3-9cd4-d62a5aa55294
ms.date: 12/05/2018
ms.keywords: GetParamText, GetParamText method [DirectShow], GetParamText method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetParamText method, IMediaParamInfo.GetParamText, IMediaParamInfo::GetParamText, IMediaParamInfoGetParamText, dshow.imediaparaminfo_getparamtext, medparam/IMediaParamInfo::GetParamText
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaParamInfo::GetParamText
 - medparam/IMediaParamInfo::GetParamText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParamInfo.GetParamText
---

# IMediaParamInfo::GetParamText


## -description

The <code>GetParamText</code> method retrieves a series of text strings that describe the parameter.

## -parameters

### -param dwParamIndex [in]

Zero-based index of the parameter.

### -param ppwchText [out]

Address of a variable that receives a pointer to a series of Unicode™ strings.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -remarks

If the method succeeds, *<i>ppwchText</i> points to a string with the following format:

<code>Name\0Unit\0Enum1\0Enum2\0...EnumN\0\0</code>

where

<ul>
<li><i>Name</i> is the name of the parameter.</li>
<li><i>Unit</i> is the name of the units; for example, milliseconds.</li>
<li><i>Enum1</i> through <i></i></li>
<li><i>EnumN</i> are descriptive names for the parameter's enumerated values. (Applies only to parameters of type MPT_ENUM.)</li>
</ul>
The application can display these values within its user interface. They are not guaranteed to follow a consistent naming scheme. If the user's computer is using an international code page, the method might return a localized string corresponding to that code page.

The object uses the <b>CoTaskMemAlloc</b> function to allocate memory for the string. After you call this method, call <b>CoTaskMemFree</b> to free the buffer.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>