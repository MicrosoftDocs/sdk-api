---
UID: NF:cryptxml.CryptXmlSetHMACSecret
title: CryptXmlSetHMACSecret function
author: windows-sdk-content
description: Sets the HMAC secret on the handle before calling the CryptXmlSign or CryptXmlVerify function.
old-location: security\cryptxmlsethmacsecret.htm
tech.root: SecCrypto
ms.assetid: 3e7d0280-c10e-4328-b7f7-208ea5a4285c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CryptXmlSetHMACSecret, CryptXmlSetHMACSecret function [Security], cryptxml/CryptXmlSetHMACSecret, security.cryptxmlsethmacsecret
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlSetHMACSecret
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptXmlSetHMACSecret function


## -description


The <b>CryptXmlSetHMACSecret</b> function sets the HMAC secret on the handle before
 calling the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> or <a href="https://msdn.microsoft.com/1f8776dc-d91a-4be9-90bf-7d36d587ffb2">CryptXmlVerify</a> function.


## -parameters




### -param hSignature [in]

The handle of the XML <b>Signature</b> element.


### -param pbSecret [in]

A pointer to a buffer that contains a block of bytes. 
    The pointer must be valid during the call to the <a href="https://msdn.microsoft.com/38bd365e-bc63-498c-a650-471429f09d37">CryptXmlSign</a> or <a href="https://msdn.microsoft.com/1f8776dc-d91a-4be9-90bf-7d36d587ffb2">CryptXmlVerify</a> function.


### -param cbSecret

The size, in bytes, of the buffer pointed to by the <i>pbSecret</i> parameter. 


## -returns



If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.



