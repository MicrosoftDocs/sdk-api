---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
title: PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
author: windows-driver-content
description: The CertStoreProvSetCTLProperty callback function determines whether a property can be set on a CTL.
old-location: security\certstoreprovsetctlproperty.htm
old-project: SecCrypto
ms.assetid: d062c875-b8c1-454f-8a0d-2ada74e5028d
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: CertStoreProvSetCTLProperty, CertStoreProvSetCTLProperty callback, CertStoreProvSetCTLProperty callback function [Security], PFN_CERT_STORE_PROV_SET_CTL_PROPERTY, PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function [Security], _crypto2_certstoreprovsetctlproperty, security.certstoreprovsetctlproperty, wincrypt/CertStoreProvSetCTLProperty, wincrypt/PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
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
-	CertStoreProvSetCTLProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function


## -description



			The <b>CertStoreProvSetCTLProperty</b> callback function determines whether a property can be set on a CTL. It is called by 
<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a> before setting a CTL's property. It can also be called by 
<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>, when getting a hash property that needs to be created and then persisted. This callback function does not set the 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>'s property.


## -parameters




### -param hStoreProv [in]

A handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param pCtlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure.


### -param dwPropId [in]

Identifier of the property to be set.


### -param dwFlags [in]

Any needed flag values.


### -param *pvData [in]

A pointer to a buffer containing the property value to be set.


## -returns




						Returns <b>TRUE</b> if the property can be set. Returns <b>FALSE</b> if the property cannot be set.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/16e45fe1-2710-4fa1-82da-c298645d7379">CertGetCTLContextProperty</a>



<a href="https://msdn.microsoft.com/3af01ca6-6fa1-4510-872a-b5e13e07f49f">CertSetCTLContextProperty</a>
 

 

