---
UID: NF:mfidl.IMFContentDecryptorContext.InitializeHardwareKey
title: IMFContentDecryptorContext::InitializeHardwareKey
author: windows-sdk-content
description: Allows the display driver to return IHV-specific information used when initializing a new hardware key.
old-location: mf\imfcontentdecryptorcontext_initializehardwarekey.htm
tech.root: medfound
ms.assetid: E1F12329-9BA5-4765-8C4A-1678C5F9E5F8
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IMFContentDecryptorContext interface [Media Foundation],InitializeHardwareKey method, IMFContentDecryptorContext.InitializeHardwareKey, IMFContentDecryptorContext::InitializeHardwareKey, InitializeHardwareKey, InitializeHardwareKey method [Media Foundation], InitializeHardwareKey method [Media Foundation],IMFContentDecryptorContext interface, mf.imfcontentdecryptorcontext_initializehardwarekey, mfidl/IMFContentDecryptorContext::InitializeHardwareKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - COM
api_location:
 - mfplat.dll
api_name:
 - IMFContentDecryptorContext.InitializeHardwareKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentDecryptorContext::InitializeHardwareKey


## -description


 Allows the display driver to return IHV-specific information used when initializing a new hardware key. 


## -parameters




### -param InputPrivateDataByteCount [in]

The number of bytes in the buffer that <i>InputPrivateData</i> specifies.


### -param InputPrivateData [in, optional]

The contents of this parameter are defined by the implementation of   
         the protection system that runs in the security processor. The contents may contain data about license or stream properties.


### -param OutputPrivateData [out]

The return data is also defined by the implementation of the protection system implementation   
     that runs in the security processor.  The contents may contain data associated with the underlying hardware key.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/94DB835F-3D2A-4CC8-A1CF-10215E3D30D6">IMFContentDecryptorContext</a>
 

 

