---
UID: NF:msctf.ITfRange.GetEmbedded
title: ITfRange::GetEmbedded (msctf.h)
description: The ITfRange::GetEmbedded method obtains content that corresponds to a TS_CHAR_EMBEDDED character in the text stream. The start anchor of the range of text is positioned just before the character of interest.
helpviewer_keywords: ["Caller-defined","GUID_TS_SERVICE_ACCESSIBLE","GUID_TS_SERVICE_ACTIVEX","GUID_TS_SERVICE_DATAOBJECT","GetEmbedded","GetEmbedded method [Text Services Framework]","GetEmbedded method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","GetEmbedded method","ITfRange.GetEmbedded","ITfRange::GetEmbedded","_tsf_itfrange_getembedded_ref","msctf/ITfRange::GetEmbedded","tsf.itfrange_getembedded"]
old-location: tsf\itfrange_getembedded.htm
tech.root: TSF
ms.assetid: ff8c4f60-76d5-422d-9d23-584e8eb5f1a1
ms.date: 12/05/2018
ms.keywords: Caller-defined, GUID_TS_SERVICE_ACCESSIBLE, GUID_TS_SERVICE_ACTIVEX, GUID_TS_SERVICE_DATAOBJECT, GetEmbedded, GetEmbedded method [Text Services Framework], GetEmbedded method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetEmbedded method, ITfRange.GetEmbedded, ITfRange::GetEmbedded, _tsf_itfrange_getembedded_ref, msctf/ITfRange::GetEmbedded, tsf.itfrange_getembedded
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfRange::GetEmbedded
 - msctf/ITfRange::GetEmbedded
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.GetEmbedded
---

# ITfRange::GetEmbedded


## -description

The <b>ITfRange::GetEmbedded</b> method obtains content that corresponds to a <a href="/windows/desktop/TSF/ts-char--constants">TS_CHAR_EMBEDDED</a> character in the text stream. The start anchor of the range of text is positioned just before the character of interest.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param rguidService [in]

Identifier that specifies how the embedded content is obtained.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACCESSIBLE"></a><a id="guid_ts_service_accessible"></a><dl>
<dt><b>GUID_TS_SERVICE_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
Output should be an <a href="/windows/desktop/WinAuto/accessible-objects">Accessible object</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_ACTIVEX"></a><a id="guid_ts_service_activex"></a><dl>
<dt><b>GUID_TS_SERVICE_ACTIVEX</b></dt>
</dl>
</td>
<td width="60%">
Caller requires a direct pointer to the object that supports the interface specified by <i>riid</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TS_SERVICE_DATAOBJECT"></a><a id="guid_ts_service_dataobject"></a><dl>
<dt><b>GUID_TS_SERVICE_DATAOBJECT</b></dt>
</dl>
</td>
<td width="60%">
Content should be obtained as an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> data transfer object, with <i>riid</i> being IID_IDataObject. Clients should specify this option when a copy of the content is required.

</td>
</tr>
<tr>
<td width="40%"><a id="Caller-defined"></a><a id="caller-defined"></a><a id="CALLER-DEFINED"></a><dl>
<dt><b>Caller-defined</b></dt>
</dl>
</td>
<td width="60%">
Text services and context owners can define custom GUIDs.

</td>
</tr>
</table>

### -param riid [in]

UUID of the interface of the requested object.

### -param ppunk [out]

Pointer to the object. It can be cast to match <i>riid</i>.

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
<dt><b>TF_E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value in the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The start anchor of the range is not positioned before a TF_CHAR_EMBEDDED character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOSERVICE</b></dt>
</dl>
</td>
<td width="60%">
The content cannot be returned to match <i>rguidService</i>.

</td>
</tr>
</table>

## -remarks

While the obtained object might not support certain interfaces, it is likely that the object will support those interfaces associated with embedded documents or controls such as <b>IOleObject</b>, <b>IDataObject</b>, <b>IViewObject</b>, <b>IPersistStorage</b>, <b>IOleCache</b>, or <b>IDispatch</b>. The caller must use <b>QueryInterface</b> to probe for any interesting interface. If the method succeeds but <i>riid</i> is <b>NULL</b>, the application indicates the presence of an embedded object but does not expose the object itself. Text processors can still benefit from a notification about the potential word break.

## -see-also

<a href="/windows/desktop/WinAuto/accessible-objects">Accessible Objects</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded">ITfRange::InsertEmbedded
      </a>



<a href="/windows/desktop/TSF/miscellaneous-framework-constants">Miscellaneous Framework Constants</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>