---
UID: NF:mfidl.IMFMediaTypeHandler.GetMediaTypeCount
title: IMFMediaTypeHandler::GetMediaTypeCount (mfidl.h)
description: Retrieves the number of media types in the object's list of supported media types.
helpviewer_keywords: ["GetMediaTypeCount","GetMediaTypeCount method [Media Foundation]","GetMediaTypeCount method [Media Foundation]","IMFMediaTypeHandler interface","IMFMediaTypeHandler interface [Media Foundation]","GetMediaTypeCount method","IMFMediaTypeHandler.GetMediaTypeCount","IMFMediaTypeHandler::GetMediaTypeCount","c5ee41bc-ee8b-4990-ae9d-92ef54597f31","mf.imfmediatypehandler_getmediatypecount","mfidl/IMFMediaTypeHandler::GetMediaTypeCount"]
old-location: mf\imfmediatypehandler_getmediatypecount.htm
tech.root: mf
ms.assetid: c5ee41bc-ee8b-4990-ae9d-92ef54597f31
ms.date: 12/05/2018
ms.keywords: GetMediaTypeCount, GetMediaTypeCount method [Media Foundation], GetMediaTypeCount method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMediaTypeCount method, IMFMediaTypeHandler.GetMediaTypeCount, IMFMediaTypeHandler::GetMediaTypeCount, c5ee41bc-ee8b-4990-ae9d-92ef54597f31, mf.imfmediatypehandler_getmediatypecount, mfidl/IMFMediaTypeHandler::GetMediaTypeCount
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
 - IMFMediaTypeHandler::GetMediaTypeCount
 - mfidl/IMFMediaTypeHandler::GetMediaTypeCount
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
 - IMFMediaTypeHandler.GetMediaTypeCount
---

# IMFMediaTypeHandler::GetMediaTypeCount


## -description

Retrieves the number of media types in the object's list of supported media types.

## -parameters

### -param pdwTypeCount [out]

Receives the number of media types in the list.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the supported media types, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex">IMFMediaTypeHandler::GetMediaTypeByIndex</a>.
      

For a media source, the media type handler for each stream must contain at least one supported media type. For media sinks, the media type handler for each stream might contain zero media types. In that case, the application must provide the media type. To test whether a particular media type is supported, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported">IMFMediaTypeHandler::IsMediaTypeSupported</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a>