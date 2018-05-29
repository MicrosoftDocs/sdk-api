---
UID: NF:mbnapi.IMbnSmsReadMsgTextCdma.get_Address
title: IMbnSmsReadMsgTextCdma::get_Address
author: windows-sdk-content
description: The mobile number associated with a message.
old-location: mbn\imbnsmsreadmsgtextcdma_address.htm
old-project: mbn
ms.assetid: e2cb5e6e-0cfa-4226-85fe-0162cf99a80f
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: Address property [Microsoft Broadband Networks], Address property [Microsoft Broadband Networks],IMbnSmsReadMsgTextCdma interface, IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks],Address property, IMbnSmsReadMsgTextCdma.Address, IMbnSmsReadMsgTextCdma.get_Address, IMbnSmsReadMsgTextCdma::Address, IMbnSmsReadMsgTextCdma::get_Address, get_Address, mbn.imbnsmsreadmsgtextcdma_address, mbnapi/IMbnSmsReadMsgTextCdma::Address, mbnapi/IMbnSmsReadMsgTextCdma::get_Address
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsReadMsgTextCdma.Address
-	IMbnSmsReadMsgTextCdma.get_Address
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsReadMsgTextCdma::get_Address


## -description


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




<a href="https://msdn.microsoft.com/d26b09f7-eb83-46ed-82cb-a702d3af5d05">IMbnSmsReadMsgTextCdma</a>
 

 

