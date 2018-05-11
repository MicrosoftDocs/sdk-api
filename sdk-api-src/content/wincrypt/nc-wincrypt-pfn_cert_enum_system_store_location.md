---
UID: NC:wincrypt.PFN_CERT_ENUM_SYSTEM_STORE_LOCATION
title: PFN_CERT_ENUM_SYSTEM_STORE_LOCATION
author: windows-driver-content
description: The CertEnumSystemStoreLocationCallback callback function formats and presents information on each system store location found by a call to CertEnumSystemStoreLocation.
old-location: security\certenumsystemstorelocationcallback.htm
old-project: SecCrypto
ms.assetid: a5f1badd-3e68-4e0f-9a42-1b1876c9cb56
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CertEnumSystemStoreLocationCallback, CertEnumSystemStoreLocationCallback callback function [Security], PFN_CERT_ENUM_SYSTEM_STORE_LOCATION, PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback, security.certenumsystemstorelocationcallback, wincrypt/CertEnumSystemStoreLocationCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: wincrypt.h
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Wincrypt.h
api_name:
-	CertEnumSystemStoreLocationCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CERT_ENUM_SYSTEM_STORE_LOCATION callback function


## -description


The <b>CertEnumSystemStoreLocationCallback</b> 
	callback function formats and presents information on each system store location found by a call to 
	<a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>.


## -parameters




### -param pwszStoreLocation [in]

String that contains information on the store location found.


### -param dwFlags [in]

Flag used to call for an alteration of the presentation.


### -param *pvReserved [in]

Reserved for future use.


### -param *pvArg [in]

A pointer to information passed to the callback function in the <i>pvArg</i> 
	 passed to <a href="https://msdn.microsoft.com/86408e6f-0732-4cb4-85cd-840b9d98b973">CertEnumSystemStoreLocation</a>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>.



