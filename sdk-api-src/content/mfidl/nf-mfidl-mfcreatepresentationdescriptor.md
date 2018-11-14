---
UID: NF:mfidl.MFCreatePresentationDescriptor
title: MFCreatePresentationDescriptor function
author: windows-sdk-content
description: Creates a presentation descriptor.
old-location: mf\mfcreatepresentationdescriptor.htm
tech.root: medfound
ms.assetid: 288ab078-5490-41a2-a3b5-87a97aa57739
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 288ab078-5490-41a2-a3b5-87a97aa57739, MFCreatePresentationDescriptor, MFCreatePresentationDescriptor function [Media Foundation], mf.mfcreatepresentationdescriptor, mfidl/MFCreatePresentationDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFCreatePresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFCreatePresentationDescriptor
: 
---

# MFCreatePresentationDescriptor function


## -description



Creates a presentation descriptor.




## -parameters




### -param cStreamDescriptors

Number of elements in the <i>apStreamDescriptors</i> array.


### -param apStreamDescriptors

Array of <a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a> interface pointers. Each pointer represents a stream descriptor for one stream in the presentation.


### -param ppPresentationDescriptor

Receives a pointer to an <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the presentation descriptor. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If you are writing a custom media source, you can use this function to create the source presentation descriptor. The presentation descriptor is created with no streams selected. Generally, a media source should select at least one stream by default. To select a stream, call <a href="https://msdn.microsoft.com/3f0eaace-9d85-4999-bb3f-34c268dfea2c">IMFPresentationDescriptor::SelectStream</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

