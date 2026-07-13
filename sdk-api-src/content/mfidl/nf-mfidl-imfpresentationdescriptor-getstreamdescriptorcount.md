---
UID: NF:mfidl.IMFPresentationDescriptor.GetStreamDescriptorCount
title: IMFPresentationDescriptor::GetStreamDescriptorCount (mfidl.h)
description: Retrieves the number of stream descriptors in the presentation. Each stream descriptor contains information about one stream in the media source. To retrieve a stream descriptor, call the IMFPresentationDescriptor::GetStreamDescriptorByIndex method.
helpviewer_keywords: ["GetStreamDescriptorCount","GetStreamDescriptorCount method [Media Foundation]","GetStreamDescriptorCount method [Media Foundation]","IMFPresentationDescriptor interface","IMFPresentationDescriptor interface [Media Foundation]","GetStreamDescriptorCount method","IMFPresentationDescriptor.GetStreamDescriptorCount","IMFPresentationDescriptor::GetStreamDescriptorCount","a01b8f91-b42a-4910-8afb-6134f5f65759","mf.imfpresentationdescriptor_getstreamdescriptorcount","mfidl/IMFPresentationDescriptor::GetStreamDescriptorCount"]
old-location: mf\imfpresentationdescriptor_getstreamdescriptorcount.htm
tech.root: mf
ms.assetid: a01b8f91-b42a-4910-8afb-6134f5f65759
ms.date: 12/05/2018
ms.keywords: GetStreamDescriptorCount, GetStreamDescriptorCount method [Media Foundation], GetStreamDescriptorCount method [Media Foundation],IMFPresentationDescriptor interface, IMFPresentationDescriptor interface [Media Foundation],GetStreamDescriptorCount method, IMFPresentationDescriptor.GetStreamDescriptorCount, IMFPresentationDescriptor::GetStreamDescriptorCount, a01b8f91-b42a-4910-8afb-6134f5f65759, mf.imfpresentationdescriptor_getstreamdescriptorcount, mfidl/IMFPresentationDescriptor::GetStreamDescriptorCount
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
 - IMFPresentationDescriptor::GetStreamDescriptorCount
 - mfidl/IMFPresentationDescriptor::GetStreamDescriptorCount
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
 - IMFPresentationDescriptor.GetStreamDescriptorCount
---

# IMFPresentationDescriptor::GetStreamDescriptorCount


## -description

Retrieves the number of stream descriptors in the presentation. Each stream descriptor contains information about one stream in the media source. To retrieve a stream descriptor, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex">IMFPresentationDescriptor::GetStreamDescriptorByIndex</a> method.

## -parameters

### -param pdwDescriptorCount [out]

Receives the number of stream descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>