---
UID: NF:mfidl.IMFMediaTypeHandler.GetMediaTypeByIndex
title: IMFMediaTypeHandler::GetMediaTypeByIndex (mfidl.h)
description: Retrieves a media type from the object's list of supported media types.
helpviewer_keywords: ["GetMediaTypeByIndex","GetMediaTypeByIndex method [Media Foundation]","GetMediaTypeByIndex method [Media Foundation]","IMFMediaTypeHandler interface","IMFMediaTypeHandler interface [Media Foundation]","GetMediaTypeByIndex method","IMFMediaTypeHandler.GetMediaTypeByIndex","IMFMediaTypeHandler::GetMediaTypeByIndex","a1827675-bbc4-45d8-8c6e-644b0d2addd4","mf.imfmediatypehandler_getmediatypebyindex","mfidl/IMFMediaTypeHandler::GetMediaTypeByIndex"]
old-location: mf\imfmediatypehandler_getmediatypebyindex.htm
tech.root: medfound
ms.assetid: a1827675-bbc4-45d8-8c6e-644b0d2addd4
ms.date: 12/05/2018
ms.keywords: GetMediaTypeByIndex, GetMediaTypeByIndex method [Media Foundation], GetMediaTypeByIndex method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMediaTypeByIndex method, IMFMediaTypeHandler.GetMediaTypeByIndex, IMFMediaTypeHandler::GetMediaTypeByIndex, a1827675-bbc4-45d8-8c6e-644b0d2addd4, mf.imfmediatypehandler_getmediatypebyindex, mfidl/IMFMediaTypeHandler::GetMediaTypeByIndex
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
 - IMFMediaTypeHandler::GetMediaTypeByIndex
 - mfidl/IMFMediaTypeHandler::GetMediaTypeByIndex
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
 - IMFMediaTypeHandler.GetMediaTypeByIndex
---

# IMFMediaTypeHandler::GetMediaTypeByIndex


## -description

Retrieves a media type from the object's list of supported media types.

## -parameters

### -param dwIndex [in]

Zero-based index of the media type to retrieve. To get the number of media types in the list, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount">IMFMediaTypeHandler::GetMediaTypeCount</a>.

### -param ppType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface. The caller must release the interface.

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
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwIndex</i> parameter is out of range.
              

</td>
</tr>
</table>

## -remarks

Media types are returned in the approximate order of preference. The list of supported types is not guaranteed to be complete. To test whether a particular media type is supported, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported">IMFMediaTypeHandler::IsMediaTypeSupported</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a>