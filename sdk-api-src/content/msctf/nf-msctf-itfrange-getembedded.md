---
UID: NF:msctf.ITfRange.GetEmbedded
title: ITfRange::GetEmbedded
author: windows-sdk-content
description: The ITfRange::GetEmbedded method obtains content that corresponds to a TS_CHAR_EMBEDDED character in the text stream. The start anchor of the range of text is positioned just before the character of interest.
old-location: tsf\itfrange_getembedded.htm
tech.root: TSF
ms.assetid: ff8c4f60-76d5-422d-9d23-584e8eb5f1a1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Caller-defined, GUID_TS_SERVICE_ACCESSIBLE, GUID_TS_SERVICE_ACTIVEX, GUID_TS_SERVICE_DATAOBJECT, GetEmbedded, GetEmbedded method [Text Services Framework], GetEmbedded method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetEmbedded method, ITfRange.GetEmbedded, ITfRange::GetEmbedded, _tsf_itfrange_getembedded_ref, msctf/ITfRange::GetEmbedded, tsf.itfrange_getembedded
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.GetEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfRange::GetEmbedded


## -description


The <b>ITfRange::GetEmbedded</b> method obtains content that corresponds to a <a href="https://msdn.microsoft.com/b40ca931-d45c-4101-9380-bb2b3ad25fba">TS_CHAR_EMBEDDED</a> character in the text stream. The start anchor of the range of text is positioned just before the character of interest.


## -parameters




### -param ec [in]

Edit cookie obtained from <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a> or <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


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
Output should be an <a href="https://msdn.microsoft.com/en-us/library/Dd317981(v=VS.85).aspx">Accessible object</a>.

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
Content should be obtained as an <a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> data transfer object, with <i>riid</i> being IID_IDataObject. Clients should specify this option when a copy of the content is required.

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




<a href="https://msdn.microsoft.com/en-us/library/Dd317981(v=VS.85).aspx">Accessible Objects</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a>



<a href="https://msdn.microsoft.com/95b8622d-c934-4293-abb4-9eface451be5">ITfRange::InsertEmbedded
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



<a href="https://msdn.microsoft.com/c827999a-0b74-4e5d-901e-4c2fa1d74929">Text Stores</a>
 

 

