---
UID: NF:mfidl.IMFMediaTypeHandler.IsMediaTypeSupported
title: IMFMediaTypeHandler::IsMediaTypeSupported (mfidl.h)
description: Queries whether the object supports a specified media type.
helpviewer_keywords: ["IMFMediaTypeHandler interface [Media Foundation]","IsMediaTypeSupported method","IMFMediaTypeHandler.IsMediaTypeSupported","IMFMediaTypeHandler::IsMediaTypeSupported","IsMediaTypeSupported","IsMediaTypeSupported method [Media Foundation]","IsMediaTypeSupported method [Media Foundation]","IMFMediaTypeHandler interface","ea52defa-8b78-4f40-97ae-ed6a5ee4849e","mf.imfmediatypehandler_ismediatypesupported","mfidl/IMFMediaTypeHandler::IsMediaTypeSupported"]
old-location: mf\imfmediatypehandler_ismediatypesupported.htm
tech.root: mf
ms.assetid: ea52defa-8b78-4f40-97ae-ed6a5ee4849e
ms.date: 12/05/2018
ms.keywords: IMFMediaTypeHandler interface [Media Foundation],IsMediaTypeSupported method, IMFMediaTypeHandler.IsMediaTypeSupported, IMFMediaTypeHandler::IsMediaTypeSupported, IsMediaTypeSupported, IsMediaTypeSupported method [Media Foundation], IsMediaTypeSupported method [Media Foundation],IMFMediaTypeHandler interface, ea52defa-8b78-4f40-97ae-ed6a5ee4849e, mf.imfmediatypehandler_ismediatypesupported, mfidl/IMFMediaTypeHandler::IsMediaTypeSupported
req.header: mfidl.h
req.include-header: 
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
 - IMFMediaTypeHandler::IsMediaTypeSupported
 - mfidl/IMFMediaTypeHandler::IsMediaTypeSupported
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
 - IMFMediaTypeHandler.IsMediaTypeSupported
---

# IMFMediaTypeHandler::IsMediaTypeSupported


## -description

Queries whether the object supports a specified media type.

## -parameters

### -param pMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to check.

### -param ppMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the closest matching media type, or receives the value <b>NULL</b>. If non-<b>NULL</b>, the caller must release the interface. This parameter can be <b>NULL</b>. See Remarks.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this media type.
              

</td>
</tr>
</table>

## -remarks

If the object supports the media type given in <i>pMediaType</i>, the method returns <b>S_OK</b>. For a media source, it means the source can generate data that conforms to that media type. For a media sink, it means the sink can receive data that conforms to that media type. If the object does not support the media type, the method fails.
      

The <i>ppMediaType</i> parameter is optional. If the method fails, the object might use <i>ppMediaType</i> to return a media type that the object does support, and which closely matches the one given in <i>pMediaType</i>. The method is not guaranteed to return a media type in <i>ppMediaType</i>. If no type is returned, this parameter receives a <b>NULL</b> pointer. If the method succeeds, this parameter receives a <b>NULL</b> pointer. If the caller sets <i>ppMediaType</i> to <b>NULL</b>, this parameter is ignored.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with SP2 and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a>