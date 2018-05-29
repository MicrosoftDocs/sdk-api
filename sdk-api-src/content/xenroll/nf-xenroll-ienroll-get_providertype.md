---
UID: NF:xenroll.IEnroll.get_ProviderType
title: IEnroll::get_ProviderType
author: windows-sdk-content
description: Sets or retrieves the type of provider.
old-location: security\ienroll4_providertype.htm
old-project: SecCrypto
ms.assetid: d4ab2b0e-127f-4ec0-9e4a-4314561912e3
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IEnroll interface [Security],ProviderType property, IEnroll.ProviderType, IEnroll.get_ProviderType, IEnroll::ProviderType, IEnroll::get_ProviderType, IEnroll::put_ProviderType, ProviderType property [Security], ProviderType property [Security],IEnroll interface, get_ProviderType, security.ienroll4_providertype, xenroll/IEnroll::ProviderType, xenroll/IEnroll::get_ProviderType, xenroll/IEnroll::put_ProviderType
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
-	IEnroll.ProviderType
-	IEnroll.get_ProviderType
-	IEnroll.put_ProviderType
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IEnroll::get_ProviderType


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ProviderType</b> property sets or retrieves the type of provider.

The value of the <b>ProviderType</b> property is passed to the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function. Valid values are determined by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) in use. The default value for this property is 1. This property was first defined in the <a href="https://msdn.microsoft.com/5be210b8-475a-4504-9cc0-5b02384e114e">IEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



For general information about provider types, see 
<a href="https://msdn.microsoft.com/ec50d6f1-999d-4ce9-85b4-816afb17550e">Cryptographic Provider Types</a>.

For more information about valid values for the Microsoft Base Cryptographic Provider, see the 
<a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a> CryptoAPI function.

For provider type information for other CSPs, see the documentation provided with the CSP.

The <b>ProviderType</b> property value is passed to <a href="https://msdn.microsoft.com/57e13662-3189-4f8d-b90a-d1fbdc09b63c">CryptAcquireContext</a>  by using its <i>dwProvType</i> parameter.


The <b>ProviderType</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/ebbcc9ad-9f87-4abe-963b-38c57a60e45e">createPKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5edd54c5-9dfb-44b8-a293-4fe6a8de45e3">createFilePKCS10WStr</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f3b40f56-3332-44e8-9753-4107948d0801">enumProvidersWStr</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll</a>
 

 

