---
UID: NF:wincrypt.CryptMsgClose
title: CryptMsgClose function
author: windows-sdk-content
description: The CryptMsgClose function closes a cryptographic message handle. At each call to this function, the reference count on the message is reduced by one. When the reference count reaches zero, the message is fully released.
old-location: security\cryptmsgclose.htm
tech.root: SecCrypto
ms.assetid: 2478dd60-233a-4ef3-86e9-62d2a59ab28a
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CryptMsgClose, CryptMsgClose function [Security], _crypto2_cryptmsgclose, security.cryptmsgclose, wincrypt/CryptMsgClose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptMsgClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptMsgClose function


## -description


The <b>CryptMsgClose</b> function closes a cryptographic message handle. At each call to this function, the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the message is reduced by one. When the reference count reaches zero, the message is fully released.


## -parameters




### -param hCryptMsg [in]

Handle of the cryptographic message to be closed.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3df6312-c866-4faa-8b89-bda67c697631">CryptMsgOpenToDecode</a>



<a href="https://msdn.microsoft.com/b0d2610b-05ba-4fb6-8f38-10f970a52091">CryptMsgOpenToEncode</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Low-level Message Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Simplified Message Functions</a>
 

 

