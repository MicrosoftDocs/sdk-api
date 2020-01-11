---
UID: NF:mbnapi.IMbnSmsReadMsgTextCdma.get_Address
title: IMbnSmsReadMsgTextCdma::get_Address (mbnapi.h)
description: The mobile number associated with a message.
old-location: mbn\imbnsmsreadmsgtextcdma_address.htm
tech.root: mbn
ms.assetid: e2cb5e6e-0cfa-4226-85fe-0162cf99a80f
ms.date: 12/05/2018
ms.keywords: Address property [Microsoft Broadband Networks], Address property [Microsoft Broadband Networks],IMbnSmsReadMsgTextCdma interface, IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks],Address property, IMbnSmsReadMsgTextCdma.Address, IMbnSmsReadMsgTextCdma.get_Address, IMbnSmsReadMsgTextCdma::Address, IMbnSmsReadMsgTextCdma::get_Address, get_Address, mbn.imbnsmsreadmsgtextcdma_address, mbnapi/IMbnSmsReadMsgTextCdma::Address, mbnapi/IMbnSmsReadMsgTextCdma::get_Address
f1_keywords:
- mbnapi/IMbnSmsReadMsgTextCdma.Address
dev_langs:
- c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mbnapi.h
api_name:
- IMbnSmsReadMsgTextCdma.Address
- IMbnSmsReadMsgTextCdma.get_Address
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSmsReadMsgTextCdma::get_Address


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

The mobile number associated with a message.

This property is read-only.


## -parameters


## -remarks



For a received message, this is the sender's number.  For a sent or draft message, this is the receiver's number.


The <i>address</i> can be in either of these formats.

<ul>
<li>"+ &lt;International Country Code&gt; &lt;SMS Service Center Number&gt;\0"</li>
<li>"&lt;SMS Service Center Number&gt;\0"</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbnsmsreadmsgtextcdma">IMbnSmsReadMsgTextCdma</a>
 

 

