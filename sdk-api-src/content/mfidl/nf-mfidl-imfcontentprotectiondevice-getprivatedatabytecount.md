---
UID: NF:mfidl.IMFContentProtectionDevice.GetPrivateDataByteCount
title: IMFContentProtectionDevice::GetPrivateDataByteCount
author: windows-sdk-content
description: Gets the required number of bytes that need to be prepended to the input and output buffers when you call the security processor through the InvokeFunction method.
old-location: mf\imfcontentprotectiondevice_getprivatedatabytecount.htm
tech.root: medfound
ms.assetid: 24FBA7E0-1496-4921-91C7-69E9AF830586
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: GetPrivateDataByteCount, GetPrivateDataByteCount method [Media Foundation], GetPrivateDataByteCount method [Media Foundation],IMFContentProtectionDevice interface, IMFContentProtectionDevice interface [Media Foundation],GetPrivateDataByteCount method, IMFContentProtectionDevice.GetPrivateDataByteCount, IMFContentProtectionDevice::GetPrivateDataByteCount, mf.imfcontentprotectiondevice_getprivatedatabytecount, mfidl/IMFContentProtectionDevice::GetPrivateDataByteCount
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
 - IMFContentProtectionDevice.GetPrivateDataByteCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentProtectionDevice::GetPrivateDataByteCount


## -description


     Gets the required number of bytes that need to be prepended to   
     the  input and output buffers when you call the security processor through the <a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">InvokeFunction</a> method.  
     When you specify this number of bytes, the Media Foundation transform (MFT) decryptor can allocate the total amount of bytes and can avoid making copies of the data when the decrytor moves the data to the security processor.  


## -parameters




### -param PrivateInputByteCount [out]

The required number of bytes that need to be prepended to   
      the input buffer that you supply to content protection system.


### -param PrivateOutputByteCount [out]

The required number of bytes that need to be prepended to   
           the output buffer that you supply to content protection system.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/A95F6526-60D2-4922-897E-6369EBB0DC79">IMFContentProtectionDevice</a>



<a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">InvokeFunction</a>
 

 

