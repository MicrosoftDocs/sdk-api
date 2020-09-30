---
UID: NF:mfobjects.IMFMediaType.GetMajorType
title: IMFMediaType::GetMajorType (mfobjects.h)
description: Gets the major type of the format.
helpviewer_keywords: ["98f0a9ca-4766-4d2b-89b8-d6e30b75f47d","GetMajorType","GetMajorType method [Media Foundation]","GetMajorType method [Media Foundation]","IMFMediaType interface","IMFMediaType interface [Media Foundation]","GetMajorType method","IMFMediaType.GetMajorType","IMFMediaType::GetMajorType","mf.imfmediatype_getmajortype","mfobjects/IMFMediaType::GetMajorType"]
old-location: mf\imfmediatype_getmajortype.htm
tech.root: mf
ms.assetid: 98f0a9ca-4766-4d2b-89b8-d6e30b75f47d
ms.date: 12/05/2018
ms.keywords: 98f0a9ca-4766-4d2b-89b8-d6e30b75f47d, GetMajorType, GetMajorType method [Media Foundation], GetMajorType method [Media Foundation],IMFMediaType interface, IMFMediaType interface [Media Foundation],GetMajorType method, IMFMediaType.GetMajorType, IMFMediaType::GetMajorType, mf.imfmediatype_getmajortype, mfobjects/IMFMediaType::GetMajorType
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
 - IMFMediaType::GetMajorType
 - mfobjects/IMFMediaType::GetMajorType
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
 - IMFMediaType.GetMajorType
---

# IMFMediaType::GetMajorType


## -description

Gets the major type of the format.

## -parameters

### -param pguidMajorType [out]

Receives the major type <b>GUID</b>. The major type describes the broad category of the format, such as audio or video. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

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
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The major type is not set.
              

</td>
</tr>
</table>

## -remarks

This method is equivalent to getting the <a href="/windows/desktop/medfound/mf-mt-major-type-attribute">MF_MT_MAJOR_TYPE</a> attribute from the media type.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>