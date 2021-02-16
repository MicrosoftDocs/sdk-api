---
UID: NF:mfidl.IMFMediaSourcePresentationProvider.ForceEndOfPresentation
title: IMFMediaSourcePresentationProvider::ForceEndOfPresentation (mfidl.h)
description: Notifies the source when playback has reached the end of a segment. For timelines, this corresponds to reaching a mark-out point.
helpviewer_keywords: ["ForceEndOfPresentation","ForceEndOfPresentation method [Media Foundation]","ForceEndOfPresentation method [Media Foundation]","IMFMediaSourcePresentationProvider interface","IMFMediaSourcePresentationProvider interface [Media Foundation]","ForceEndOfPresentation method","IMFMediaSourcePresentationProvider.ForceEndOfPresentation","IMFMediaSourcePresentationProvider::ForceEndOfPresentation","fb2896f9-c397-4a0d-b8fe-b03ff4f08dda","mf.imfmediasourcepresentationprovider_forceendofpresentation","mfidl/IMFMediaSourcePresentationProvider::ForceEndOfPresentation"]
old-location: mf\imfmediasourcepresentationprovider_forceendofpresentation.htm
tech.root: mf
ms.assetid: fb2896f9-c397-4a0d-b8fe-b03ff4f08dda
ms.date: 12/05/2018
ms.keywords: ForceEndOfPresentation, ForceEndOfPresentation method [Media Foundation], ForceEndOfPresentation method [Media Foundation],IMFMediaSourcePresentationProvider interface, IMFMediaSourcePresentationProvider interface [Media Foundation],ForceEndOfPresentation method, IMFMediaSourcePresentationProvider.ForceEndOfPresentation, IMFMediaSourcePresentationProvider::ForceEndOfPresentation, fb2896f9-c397-4a0d-b8fe-b03ff4f08dda, mf.imfmediasourcepresentationprovider_forceendofpresentation, mfidl/IMFMediaSourcePresentationProvider::ForceEndOfPresentation
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
 - IMFMediaSourcePresentationProvider::ForceEndOfPresentation
 - mfidl/IMFMediaSourcePresentationProvider::ForceEndOfPresentation
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
 - IMFMediaSourcePresentationProvider.ForceEndOfPresentation
---

# IMFMediaSourcePresentationProvider::ForceEndOfPresentation


## -description

Notifies the source when playback has reached the end of a segment. For timelines, this corresponds to reaching a mark-out point.

## -parameters

### -param pPresentationDescriptor [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor for the segment that has ended.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider">IMFMediaSourcePresentationProvider</a>