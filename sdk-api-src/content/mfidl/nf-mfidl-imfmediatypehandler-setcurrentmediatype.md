---
UID: NF:mfidl.IMFMediaTypeHandler.SetCurrentMediaType
title: IMFMediaTypeHandler::SetCurrentMediaType (mfidl.h)
description: Sets the object's media type.
helpviewer_keywords: ["77ff397e-4fa8-4849-98b8-6bdd035c0e89","IMFMediaTypeHandler interface [Media Foundation]","SetCurrentMediaType method","IMFMediaTypeHandler.SetCurrentMediaType","IMFMediaTypeHandler::SetCurrentMediaType","SetCurrentMediaType","SetCurrentMediaType method [Media Foundation]","SetCurrentMediaType method [Media Foundation]","IMFMediaTypeHandler interface","mf.imfmediatypehandler_setcurrentmediatype","mfidl/IMFMediaTypeHandler::SetCurrentMediaType"]
old-location: mf\imfmediatypehandler_setcurrentmediatype.htm
tech.root: mf
ms.assetid: 77ff397e-4fa8-4849-98b8-6bdd035c0e89
ms.date: 12/05/2018
ms.keywords: 77ff397e-4fa8-4849-98b8-6bdd035c0e89, IMFMediaTypeHandler interface [Media Foundation],SetCurrentMediaType method, IMFMediaTypeHandler.SetCurrentMediaType, IMFMediaTypeHandler::SetCurrentMediaType, SetCurrentMediaType, SetCurrentMediaType method [Media Foundation], SetCurrentMediaType method [Media Foundation],IMFMediaTypeHandler interface, mf.imfmediatypehandler_setcurrentmediatype, mfidl/IMFMediaTypeHandler::SetCurrentMediaType
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
 - IMFMediaTypeHandler::SetCurrentMediaType
 - mfidl/IMFMediaTypeHandler::SetCurrentMediaType
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
 - IMFMediaTypeHandler.SetCurrentMediaType
---

# IMFMediaTypeHandler::SetCurrentMediaType


## -description

Sets the object's media type.

## -parameters

### -param pMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the new media type.

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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid request.
              

</td>
</tr>
</table>

## -remarks

For media sources, setting the media type means the source will generate data that conforms to that media type. For media sinks, setting the media type means the sink can receive data that conforms to that media type.

Any implementation of this method should check whether <i>pMediaType</i> differs from the object's current media type. If the types are identical, the method should return S_OK but avoid releasing and recreating resources unnecessarily. If the types are not identical, the method should validate the new type.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a>