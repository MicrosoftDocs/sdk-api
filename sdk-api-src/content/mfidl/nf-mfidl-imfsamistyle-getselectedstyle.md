---
UID: NF:mfidl.IMFSAMIStyle.GetSelectedStyle
title: IMFSAMIStyle::GetSelectedStyle (mfidl.h)
description: Gets the current style from the SAMI media source.
helpviewer_keywords: ["7501a4d5-eb5f-4f62-ae55-96ee999e561c","GetSelectedStyle","GetSelectedStyle method [Media Foundation]","GetSelectedStyle method [Media Foundation]","IMFSAMIStyle interface","IMFSAMIStyle interface [Media Foundation]","GetSelectedStyle method","IMFSAMIStyle.GetSelectedStyle","IMFSAMIStyle::GetSelectedStyle","mf.imfsamistyle_getselectedstyle","mfidl/IMFSAMIStyle::GetSelectedStyle"]
old-location: mf\imfsamistyle_getselectedstyle.htm
tech.root: mf
ms.assetid: 7501a4d5-eb5f-4f62-ae55-96ee999e561c
ms.date: 12/05/2018
ms.keywords: 7501a4d5-eb5f-4f62-ae55-96ee999e561c, GetSelectedStyle, GetSelectedStyle method [Media Foundation], GetSelectedStyle method [Media Foundation],IMFSAMIStyle interface, IMFSAMIStyle interface [Media Foundation],GetSelectedStyle method, IMFSAMIStyle.GetSelectedStyle, IMFSAMIStyle::GetSelectedStyle, mf.imfsamistyle_getselectedstyle, mfidl/IMFSAMIStyle::GetSelectedStyle
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFSAMIStyle::GetSelectedStyle
 - mfidl/IMFSAMIStyle::GetSelectedStyle
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
 - IMFSAMIStyle.GetSelectedStyle
---

# IMFSAMIStyle::GetSelectedStyle


## -description

Gets the current style from the SAMI media source.

## -parameters

### -param ppwszStyle [out]

Receives a pointer to a null-terminated string that contains the name of the style. If no style is currently set, the method returns an empty string. The caller must free the memory for the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle">IMFSAMIStyle</a>



<a href="/windows/desktop/medfound/sami-media-source">SAMI Media Source</a>