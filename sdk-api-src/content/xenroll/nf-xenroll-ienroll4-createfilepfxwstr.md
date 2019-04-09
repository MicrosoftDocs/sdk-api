---
UID: NF:xenroll.IEnroll4.createFilePFXWStr
title: IEnroll4::createFilePFXWStr (xenroll.h)
author: windows-sdk-content
description: Saves the accepted certificate chain and private key in a file in Personal Information Exchange (PFX) format.
old-location: security\ienroll4_createfilepfxwstr.htm
tech.root: SecCrypto
ms.assetid: 1df364e7-35ab-4c16-ac13-2f0be36fe0f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnroll4 interface [Security],createFilePFXWStr method, IEnroll4.createFilePFXWStr, IEnroll4::createFilePFXWStr, createFilePFXWStr, createFilePFXWStr method [Security], createFilePFXWStr method [Security],IEnroll4 interface, security.ienroll4_createfilepfxwstr, xenroll/IEnroll4::createFilePFXWStr
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll4.createFilePFXWStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnroll4::createFilePFXWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createFilePFXWStr</b> method saves the accepted certificate chain and <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> in a file in Personal Information Exchange (PFX) format. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pwszPassword [in]

A pointer to a <b>null</b>-terminated wide character string that represents the password for the PFX-format message. This value may be empty or <b>NULL</b> to indicate that no password is used. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>. For more information about protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param pwszPFXFileName [in]

A pointer to a <b>null</b>-terminated wide character string that contains the name of the file that will receive the base64-encoded PFX data.


## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

