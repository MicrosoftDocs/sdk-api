---
UID: NF:mfidl.MFCreatePresentationDescriptor
title: MFCreatePresentationDescriptor function (mfidl.h)
description: Creates a presentation descriptor.
helpviewer_keywords: ["288ab078-5490-41a2-a3b5-87a97aa57739","MFCreatePresentationDescriptor","MFCreatePresentationDescriptor function [Media Foundation]","mf.mfcreatepresentationdescriptor","mfidl/MFCreatePresentationDescriptor"]
old-location: mf\mfcreatepresentationdescriptor.htm
tech.root: mf
ms.assetid: 288ab078-5490-41a2-a3b5-87a97aa57739
ms.date: 12/05/2018
ms.keywords: 288ab078-5490-41a2-a3b5-87a97aa57739, MFCreatePresentationDescriptor, MFCreatePresentationDescriptor function [Media Foundation], mf.mfcreatepresentationdescriptor, mfidl/MFCreatePresentationDescriptor
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreatePresentationDescriptor
 - mfidl/MFCreatePresentationDescriptor
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
 - MFCreatePresentationDescriptor
---

# MFCreatePresentationDescriptor function


## -description

Creates a presentation descriptor.

## -parameters

### -param cStreamDescriptors

Number of elements in the <i>apStreamDescriptors</i> array.

### -param apStreamDescriptors

Array of <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor">IMFStreamDescriptor</a> interface pointers. Each pointer represents a stream descriptor for one stream in the presentation.

### -param ppPresentationDescriptor

Receives a pointer to an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you are writing a custom media source, you can use this function to create the source presentation descriptor. The presentation descriptor is created with no streams selected. Generally, a media source should select at least one stream by default. To select a stream, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream">IMFPresentationDescriptor::SelectStream</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/presentation-descriptors">Presentation Descriptors</a>