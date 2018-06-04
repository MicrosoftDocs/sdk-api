---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

