---
UID: NS:ntsecpkg._SECPKG_SERIALIZED_OID
title: "_SECPKG_SERIALIZED_OID"
author: windows-sdk-content
description: Contains the security package's object identifier (OID).
old-location: security\secpkg_serialized_oid.htm
old-project: secauthn
ms.assetid: 54CF931B-AD1F-4370-A2AF-5DF4BC9EA007
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSECPKG_SERIALIZED_OID, PSECPKG_SERIALIZED_OID, PSECPKG_SERIALIZED_OID structure pointer [Security], SECPKG_SERIALIZED_OID, SECPKG_SERIALIZED_OID structure [Security], _SECPKG_SERIALIZED_OID, ntsecpkg/PSECPKG_SERIALIZED_OID, ntsecpkg/SECPKG_SERIALIZED_OID, security.secpkg_serialized_oid"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: SECPKG_SERIALIZED_OID, *PSECPKG_SERIALIZED_OID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_SERIALIZED_OID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SECPKG_SERIALIZED_OID structure


## -description


The <b>SECPKG_SERIALIZED_OID</b> structure contains the security package's object identifier (OID). 

This structure is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -struct-fields




### -field OidLength

The length of the OID.


### -field OidAttributes

The attributes of the OID.


### -field OidValue

The value of the OID. The value of SECPKG_MAX_OID_LENGTH is currently set to 32.

