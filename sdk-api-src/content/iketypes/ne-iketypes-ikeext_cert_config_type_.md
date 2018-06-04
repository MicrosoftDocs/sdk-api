---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

