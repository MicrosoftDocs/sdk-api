---
UID: NE:iketypes.IKEEXT_CERT_CONFIG_TYPE_
title: IKEEXT_CERT_CONFIG_TYPE_
author: windows-sdk-content
description: Indicates a type of certificate configuration.
old-location: fwp\ikeext_cert_config_type.htm
old-project: FWP
ms.assetid: b137e27b-c361-4fd2-9b3b-5c2b364576d4
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IKEEXT_CERT_CONFIG_ENTERPRISE_STORE, IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST, IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE, IKEEXT_CERT_CONFIG_TYPE, IKEEXT_CERT_CONFIG_TYPE enumeration [Filtering], IKEEXT_CERT_CONFIG_TYPE_, IKEEXT_CERT_CONFIG_TYPE_MAX, IKEEXT_CERT_CONFIG_UNSPECIFIED, fwp.ikeext_cert_config_type, iketypes/IKEEXT_CERT_CONFIG_ENTERPRISE_STORE, iketypes/IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST, iketypes/IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE, iketypes/IKEEXT_CERT_CONFIG_TYPE, iketypes/IKEEXT_CERT_CONFIG_TYPE_MAX, iketypes/IKEEXT_CERT_CONFIG_UNSPECIFIED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_CERT_CONFIG_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_CERT_CONFIG_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_CERT_CONFIG_TYPE_ enumeration


## -description


The <b>IKEEXT_CERT_CONFIG_TYPE</b> enumerated type indicates a type of certificate configuration.


## -enum-fields




### -field IKEEXT_CERT_CONFIG_EXPLICIT_TRUST_LIST

An explicit trust list will be used for authentication.


### -field IKEEXT_CERT_CONFIG_ENTERPRISE_STORE

The enterprise store will be used as the trust list for authentication.


### -field IKEEXT_CERT_CONFIG_TRUSTED_ROOT_STORE

The trusted root CA store will be used as the trust list for authentication.


### -field IKEEXT_CERT_CONFIG_UNSPECIFIED

No certificate authentication in the direction (inbound or outbound) specified by the configuration.

Available only on Windows 7, Windows Server 2008 R2, and later.


### -field IKEEXT_CERT_CONFIG_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

