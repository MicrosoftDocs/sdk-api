---
UID: NN:mfidl.IMFContentProtectionDevice
title: IMFContentProtectionDevice (mfidl.h)
description: Allows a decryptor to communicate with the security processor that implements the hardware decryption for a protection system.
helpviewer_keywords: ["IMFContentProtectionDevice","IMFContentProtectionDevice interface [Media Foundation]","IMFContentProtectionDevice interface [Media Foundation]","described","mf.imfcontentprotectiondevice","mfidl/IMFContentProtectionDevice"]
old-location: mf\imfcontentprotectiondevice.htm
tech.root: mf
ms.assetid: A95F6526-60D2-4922-897E-6369EBB0DC79
ms.date: 12/05/2018
ms.keywords: IMFContentProtectionDevice, IMFContentProtectionDevice interface [Media Foundation], IMFContentProtectionDevice interface [Media Foundation],described, mf.imfcontentprotectiondevice, mfidl/IMFContentProtectionDevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentProtectionDevice
 - mfidl/IMFContentProtectionDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.dll
api_name:
 - IMFContentProtectionDevice
---

# IMFContentProtectionDevice interface


## -description

Allows a decryptor to communicate with the security processor that implements the hardware decryption for a protection system.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFContentProtectionDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFContentProtectionDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-getprivatedatabytecount">GetPrivateDataByteCount</a>
</td>
<td align="left" width="63%">
     Gets the required number of bytes that need to be prepended to   
     the  input and output buffers when you call the security processor through the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">InvokeFunction</a> method.  
     When you specify this number of bytes, the Media Foundation transform (MFT) decryptor can allocate the total amount of bytes and can avoid making copies of the data when the decrytor moves the data to the security processor.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectiondevice-invokefunction">InvokeFunction</a>
</td>
<td align="left" width="63%">
Calls into the implementation of the protection system in the security processor. 

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

