---
UID: NN:mfidl.IMFContentProtectionDevice
title: IMFContentProtectionDevice
author: windows-sdk-content
description: Allows a decryptor to communicate with the security processor that implements the hardware decryption for a protection system.
old-location: mf\imfcontentprotectiondevice.htm
tech.root: medfound
ms.assetid: A95F6526-60D2-4922-897E-6369EBB0DC79
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMFContentProtectionDevice, IMFContentProtectionDevice interface [Media Foundation], IMFContentProtectionDevice interface [Media Foundation],described, mf.imfcontentprotectiondevice, mfidl/IMFContentProtectionDevice
ms.topic: interface
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
 - COM
api_location:
 - mfplat.dll
api_name:
 - IMFContentProtectionDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentProtectionDevice interface


## -description


Allows a decryptor to communicate with the security processor that implements the hardware decryption for a protection system. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentProtectionDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFContentProtectionDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFContentProtectionDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24FBA7E0-1496-4921-91C7-69E9AF830586">GetPrivateDataByteCount</a>
</td>
<td align="left" width="63%">
     Gets the required number of bytes that need to be prepended to   
     the  input and output buffers when you call the security processor through the <a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">InvokeFunction</a> method.  
     When you specify this number of bytes, the Media Foundation transform (MFT) decryptor can allocate the total amount of bytes and can avoid making copies of the data when the decrytor moves the data to the security processor.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BEC7122-1DFB-49D7-BE60-7CE9D83A64F5">InvokeFunction</a>
</td>
<td align="left" width="63%">
Calls into the implementation of the protection system in the security processor. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

