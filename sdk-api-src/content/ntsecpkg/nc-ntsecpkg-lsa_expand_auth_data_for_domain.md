---
UID: NC:ntsecpkg.LSA_EXPAND_AUTH_DATA_FOR_DOMAIN
title: LSA_EXPAND_AUTH_DATA_FOR_DOMAIN
author: windows-driver-content
description: Expands the domain groups in the specified user authentication data.
old-location: security\expandauthdatafordomain.htm
old-project: SecAuthN
ms.assetid: 965d8575-a05b-45d8-8718-4004f1d22ca5
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ExpandAuthDataForDomain, ExpandAuthDataForDomain function [Security], LSA_EXPAND_AUTH_DATA_FOR_DOMAIN, ntsecpkg/ExpandAuthDataForDomain, security.expandauthdatafordomain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	ExpandAuthDataForDomain
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_EXPAND_AUTH_DATA_FOR_DOMAIN callback function


## -description


Expands the domain groups in the specified user authentication data.


## -parameters




### -param UserAuthData [in]

A pointer to the user authentication data to expand.


### -param UserAuthDataSize [in]

The size, in bytes, of the <i>UserAuthData</i> buffer.


### -param Reserved [in]

Reserved. This parameter must be set to <b>NULL.</b>


### -param *ExpandedAuthData [out]

A pointer to the expanded authentication data.


### -param ExpandedAuthDataSize [out]

A pointer to the size, in bytes, of the <i>ExpandedAuthData</i> buffer.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.




## -remarks



A pointer to the <b>ExpandAuthDataForDomain</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

