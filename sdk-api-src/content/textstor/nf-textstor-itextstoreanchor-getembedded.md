---
UID: NF:textstor.ITextStoreAnchor.GetEmbedded
title: ITextStoreAnchor::GetEmbedded (textstor.h)
description: The ITextStoreAnchor::GetEmbedded method obtains an embedded object from a text stream.
helpviewer_keywords: ["GUID_TS_SERVICE_ACCESSIBLE","GUID_TS_SERVICE_ACTIVEX","GUID_TS_SERVICE_DATAOBJECT","GetEmbedded","GetEmbedded method [Text Services Framework]","GetEmbedded method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetEmbedded method","ITextStoreAnchor.GetEmbedded","ITextStoreAnchor::GetEmbedded","textstor/ITextStoreAnchor::GetEmbedded","tsf.itextstoreanchor_getembedded"]
old-location: tsf\itextstoreanchor_getembedded.htm
tech.root: TSF
ms.assetid: 212286e1-aafa-4368-8dd3-45a0d4c6ecb9
ms.date: 12/05/2018
ms.keywords: GUID_TS_SERVICE_ACCESSIBLE, GUID_TS_SERVICE_ACTIVEX, GUID_TS_SERVICE_DATAOBJECT, GetEmbedded, GetEmbedded method [Text Services Framework], GetEmbedded method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetEmbedded method, ITextStoreAnchor.GetEmbedded, ITextStoreAnchor::GetEmbedded, textstor/ITextStoreAnchor::GetEmbedded, tsf.itextstoreanchor_getembedded
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::GetEmbedded
 - textstor/ITextStoreAnchor::GetEmbedded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.GetEmbedded
---

# ITextStoreAnchor::GetEmbedded


## -description

The <b>ITextStoreAnchor::GetEmbedded</b> method obtains an embedded object from a text stream.

## -parameters

### -param dwFlags [in]

Bit fields that specify how the method deals with hidden text. If set to TS_GEA_HIDDEN, an embedded object can be located within hidden text. Otherwise hidden text is skipped over.

### -param paPos [in]

Pointer to an anchor positioned immediately in front of the embedded object, as denoted by a TS_CHAR_EMBEDDED character.

### -param rguidService [in]

Contains a GUID value that defines the requested format of the obtained object. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_DATAOBJECT"></a><a id="guid_ts_service_dataobject"></a><dl>
<dt><b>GUID_TS_SERVICE_DATAOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> data object.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACCESSIBLE"></a><a id="guid_ts_service_accessible"></a><dl>
<dt><b>GUID_TS_SERVICE_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an <a href="/windows/desktop/WinAuto/accessible-objects">Accessible object</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACTIVEX"></a><a id="guid_ts_service_activex"></a><dl>
<dt><b>GUID_TS_SERVICE_ACTIVEX</b></dt>
</dl>
</td>
<td width="60%">
The object should be obtained as an ActiveX object.

</td>
</tr>
</table>

### -param riid [in]

Specifies the interface type requested.

### -param ppunk [out]

Pointer to an <b>IUnknown</b> pointer that receives the requested interface.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed to obtain the requested object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The implementing application does not expose embedded objects in its text stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The requested <i>paPos</i> anchor is not within the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The requested interface type is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
There is no <i>paPos</i> anchor immediately in front of a TS_CHAR_EMBEDDED character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
The service type specified in <i>rguidService</i> is unsupported.

</td>
</tr>
</table>

## -remarks

The caller must use <b>QueryInterface</b> to probe for appropriate interfaces. Prospective interfaces include those associated with embedded documents or controls such as <b>IOleObject</b>, <b>IDataObject</b>, <b>IViewObject</b>, <b>IPersistStorage</b>, <b>IOleCache</b>, or <b>IDispatch</b>.

## -see-also

<a href="/windows/desktop/WinAuto/accessible-objects">Accessible Objects</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>