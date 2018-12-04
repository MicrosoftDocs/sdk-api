---
UID: NF:mfidl.MFCreateSampleGrabberSinkActivate
title: MFCreateSampleGrabberSinkActivate function
author: windows-sdk-content
description: Creates an activation object for the sample grabber media sink.
old-location: mf\mfcreatesamplegrabbersinkactivate.htm
tech.root: medfound
ms.assetid: ac8e415e-5df8-4fdb-adf6-c3c717c3d625
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MFCreateSampleGrabberSinkActivate, MFCreateSampleGrabberSinkActivate function [Media Foundation], ac8e415e-5df8-4fdb-adf6-c3c717c3d625, mf.mfcreatesamplegrabbersinkactivate, mfidl/MFCreateSampleGrabberSinkActivate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateSampleGrabberSinkActivate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSampleGrabberSinkActivate function


## -description



Creates an activation object for the sample grabber media sink.




## -parameters




### -param pIMFMediaType

Pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface, defining the media type for the sample grabber's input stream.
          


### -param pIMFSampleGrabberSinkCallback

Pointer to the <a href="https://msdn.microsoft.com/6635823c-f532-4012-ad3c-382491b61671">IMFSampleGrabberSinkCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param ppIActivate

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface. Use this interface to complete the creation of the sample grabber. The caller must release the interface.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To create the sample grabber sink, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> on the pointer received in the <i>ppIActivate</i> parameter.

Before calling <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">ActivateObject</a>, you can configure the sample grabber by setting any of the following attributes on the <i>ppIActivate</i> pointer:

<ul>
<li>
<a href="https://msdn.microsoft.com/780ec4a6-8e14-4b81-9d50-82b2850c70ae">MF_SAMPLEGRABBERSINK_IGNORE_CLOCK</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8d06b415-aafc-4276-9a88-4b7262df62f1">MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

