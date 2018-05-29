---
UID: NF:xenroll.IEnroll4.createPFXWStr
title: IEnroll4::createPFXWStr
author: windows-sdk-content
description: Saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS #12.
old-location: security\ienroll4_createpfxwstr.htm
old-project: SecCrypto
ms.assetid: 38ab5b07-2a84-484b-b413-58f0e11599e9
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IEnroll4 interface [Security],createPFXWStr method, IEnroll4.createPFXWStr, IEnroll4::createPFXWStr, createPFXWStr, createPFXWStr method [Security], createPFXWStr method [Security],IEnroll4 interface, security.ienroll4_createpfxwstr, xenroll/IEnroll4::createPFXWStr
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: XBL_IDP_AUTH_TOKEN_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Xenroll.dll
api_name:
-	IEnroll4.createPFXWStr
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll4::createPFXWStr


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>createPFXWStr</b> method saves the accepted certificate chain and private key in a Personal Information Exchange (PFX) format string. The PFX format is also known as PKCS #12. This method was first defined in the <a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a> interface.


## -parameters




### -param pwszPassword [in]

A pointer to a null-terminated Unicode string that represents the password for the PFX-format message. This value may be empty or <b>NULL</b> to indicate that no password is used. When you have finished using the password, remove the sensitive information from memory by calling <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a>. For more information about protecting the password, see <a href="https://msdn.microsoft.com/1d810f71-9bf5-4c5c-a573-c35081f604cf">Handling Passwords</a>.


### -param pblobPFX [out]

A pointer to the <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_DATA_BLOB</a> structure  that receives the base64-encoded PFX format certificate information.

When you have finished using this memory, free it by passing the <b>pbData</b> member of this structure to the <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

