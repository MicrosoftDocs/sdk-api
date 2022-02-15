---
UID: NF:mfapi.MFCreateVideoMediaTypeFromSubtype
title: MFCreateVideoMediaTypeFromSubtype function (mfapi.h)
description: Creates a partial video media type with a specified subtype.
helpviewer_keywords: ["3ae58096-fe11-4cc8-9887-2e13f56a958d","MFCreateVideoMediaTypeFromSubtype","MFCreateVideoMediaTypeFromSubtype function [Media Foundation]","mf.mfcreatevideomediatypefromsubtype","mfapi/MFCreateVideoMediaTypeFromSubtype"]
old-location: mf\mfcreatevideomediatypefromsubtype.htm
tech.root: mf
ms.assetid: 3ae58096-fe11-4cc8-9887-2e13f56a958d
ms.date: 12/05/2018
ms.keywords: 3ae58096-fe11-4cc8-9887-2e13f56a958d, MFCreateVideoMediaTypeFromSubtype, MFCreateVideoMediaTypeFromSubtype function [Media Foundation], mf.mfcreatevideomediatypefromsubtype, mfapi/MFCreateVideoMediaTypeFromSubtype
req.header: mfapi.h
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
req.lib: Evr.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoMediaTypeFromSubtype
 - mfapi/MFCreateVideoMediaTypeFromSubtype
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreateVideoMediaTypeFromSubtype
---

# MFCreateVideoMediaTypeFromSubtype function


## -description

Creates a partial video media type with a specified subtype.

## -parameters

### -param pAMSubtype [in]

Pointer to a GUID that specifies the subtype. See <a href="/windows/desktop/medfound/video-subtype-guids">Video Subtype GUIDs</a>.

### -param ppIVideoMediaType [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype">IMFVideoMediaType</a> interface. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function creates a media type and sets the major type equal to <b>MFMediaType_Video</b> and the subtype equal to the value specified in <i>pAMSubtype</i>.
      

You can get the same result with the following steps:

<ol>
<li>Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype">MFCreateMediaType</a>. This function returns a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface.
          </li>
<li>Set the <a href="/windows/desktop/medfound/mf-mt-major-type-attribute">MF_MT_MAJOR_TYPE</a> attribute to <b>MFMediaType_Video</b>.
          </li>
<li>Set the <a href="/windows/desktop/medfound/mf-mt-subtype-attribute">MF_MT_SUBTYPE</a> attribute to the subtype.
          </li>
</ol>
<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from evr.dll. Starting in Windows 7, this function is exported from mfplat.dll, and evr.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-types">Media Types</a>