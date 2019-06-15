---
UID: NF:mfidl.MFCreateContentDecryptorContext
title: MFCreateContentDecryptorContext function (mfidl.h)
author: windows-sdk-content
description: Creates an IMFContentDecryptorContext interface for the specified media protection system.
old-location: mf\mfcreatecontentdecryptorcontext.htm
tech.root: medfound
ms.assetid: 9CD2AEAE-E960-450F-824B-ED9FD32FB210
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFCreateContentDecryptorContext, MFCreateContentDecryptorContext function [Media Foundation], mf.mfcreatecontentdecryptorcontext, mfidl/MFCreateContentDecryptorContext
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - MFCreateContentDecryptorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateContentDecryptorContext function


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext">IMFContentDecryptorContext</a> interface for the specified media protection system.  


## -parameters




### -param guidMediaProtectionSystemId [in]

The identifier of the media protection system for which you want to create an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext">IMFContentDecryptorContext</a> interface.


### -param pD3DManager [in, optional]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a> interface that you want to use for sharing the Direct3D 11 device.


### -param pContentProtectionDevice [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a> interface for the specified media protection system.


### -param ppContentDecryptorContext [out]

Pointer to the created <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext">IMFContentDecryptorContext</a> interface.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext">IMFContentDecryptorContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice">IMFContentProtectionDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager">IMFDXGIDeviceManager</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 

