---
UID: NF:mfidl.IMFMediaTypeHandler.GetMajorType
title: IMFMediaTypeHandler::GetMajorType (mfidl.h)
description: Gets the major media type of the object.
helpviewer_keywords: ["1560d113-80a9-48bb-9f3d-6e3a288db962","GetMajorType","GetMajorType method [Media Foundation]","GetMajorType method [Media Foundation]","IMFMediaTypeHandler interface","IMFMediaTypeHandler interface [Media Foundation]","GetMajorType method","IMFMediaTypeHandler.GetMajorType","IMFMediaTypeHandler::GetMajorType","mf.imfmediatypehandler_getmajortype","mfidl/IMFMediaTypeHandler::GetMajorType"]
old-location: mf\imfmediatypehandler_getmajortype.htm
tech.root: mf
ms.assetid: 1560d113-80a9-48bb-9f3d-6e3a288db962
ms.date: 12/05/2018
ms.keywords: 1560d113-80a9-48bb-9f3d-6e3a288db962, GetMajorType, GetMajorType method [Media Foundation], GetMajorType method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMajorType method, IMFMediaTypeHandler.GetMajorType, IMFMediaTypeHandler::GetMajorType, mf.imfmediatypehandler_getmajortype, mfidl/IMFMediaTypeHandler::GetMajorType
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
 - IMFMediaTypeHandler::GetMajorType
 - mfidl/IMFMediaTypeHandler::GetMajorType
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
 - IMFMediaTypeHandler.GetMajorType
---

# IMFMediaTypeHandler::GetMajorType


## -description

Gets the major media type of the object.

## -parameters

### -param pguidMajorType [out]

Receives a GUID that identifies the major type. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The major type identifies what kind of data is in the stream, such as audio or video. To get the specific details of the format, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype">IMFMediaTypeHandler::GetCurrentMediaType</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a>