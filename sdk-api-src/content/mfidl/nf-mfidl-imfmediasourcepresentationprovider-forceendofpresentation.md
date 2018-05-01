---
UID: NF:mfidl.IMFMediaSourcePresentationProvider.ForceEndOfPresentation
title: IMFMediaSourcePresentationProvider::ForceEndOfPresentation method
author: windows-driver-content
description: Notifies the source when playback has reached the end of a segment. For timelines, this corresponds to reaching a mark-out point.
old-location: mf\imfmediasourcepresentationprovider_forceendofpresentation.htm
old-project: medfound
ms.assetid: fb2896f9-c397-4a0d-b8fe-b03ff4f08dda
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: ForceEndOfPresentation method [Media Foundation], ForceEndOfPresentation method [Media Foundation], IMFMediaSourcePresentationProvider interface, ForceEndOfPresentation,IMFMediaSourcePresentationProvider.ForceEndOfPresentation, IMFMediaSourcePresentationProvider, IMFMediaSourcePresentationProvider interface [Media Foundation], ForceEndOfPresentation method, IMFMediaSourcePresentationProvider::ForceEndOfPresentation, fb2896f9-c397-4a0d-b8fe-b03ff4f08dda, mf.imfmediasourcepresentationprovider_forceendofpresentation, mfidl/IMFMediaSourcePresentationProvider::ForceEndOfPresentation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFMediaSourcePresentationProvider.ForceEndOfPresentation
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSourcePresentationProvider::ForceEndOfPresentation method


## -description



Notifies the source when playback has reached the end of a segment. For timelines, this corresponds to reaching a mark-out point.




## -parameters




### -param pPresentationDescriptor [in]

Pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the presentation descriptor for the segment that has ended.


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




<a href="https://msdn.microsoft.com/b6b36324-a315-42a0-bdbf-8d2cec6cde3f">IMFMediaSourcePresentationProvider</a>
 

 

