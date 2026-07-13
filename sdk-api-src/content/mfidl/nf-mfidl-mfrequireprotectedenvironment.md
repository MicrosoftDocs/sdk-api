---
UID: NF:mfidl.MFRequireProtectedEnvironment
title: MFRequireProtectedEnvironment function (mfidl.h)
description: Queries whether a media presentation requires the Protected Media Path (PMP).
helpviewer_keywords: ["5129d8c0-4049-4b90-ade8-b4cd32277664","MFRequireProtectedEnvironment","MFRequireProtectedEnvironment function [Media Foundation]","mf.mfrequireprotectedenvironment","mfidl/MFRequireProtectedEnvironment"]
old-location: mf\mfrequireprotectedenvironment.htm
tech.root: mf
ms.assetid: 5129d8c0-4049-4b90-ade8-b4cd32277664
ms.date: 12/05/2018
ms.keywords: 5129d8c0-4049-4b90-ade8-b4cd32277664, MFRequireProtectedEnvironment, MFRequireProtectedEnvironment function [Media Foundation], mf.mfrequireprotectedenvironment, mfidl/MFRequireProtectedEnvironment
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFRequireProtectedEnvironment
 - mfidl/MFRequireProtectedEnvironment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFRequireProtectedEnvironment
---

# MFRequireProtectedEnvironment function


## -description

Queries whether a media presentation requires the Protected Media Path (PMP).

## -parameters

### -param pPresentationDescriptor [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of a presentation descriptor. The presentation descriptor is created by the media source, and describes the presentation.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
This presentation requires a protected environment.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
This presentation does not require a protected environment.

</td>
</tr>
</table>

## -remarks

If this function returns <b>S_OK</b>, it means the PMP is required for this presentation. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession">MFCreatePMPMediaSession</a> to create the PMP session object.

If the function returns <b>S_FALSE</b>, you can use the unprotected pipeline. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession">MFCreateMediaSession</a> to create the regular Media Session object.

Internally, this function checks whether any of the stream descriptors in the presentation have the <a href="/windows/desktop/medfound/mf-sd-protected-attribute">MF_SD_PROTECTED</a> attribute with the value <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>