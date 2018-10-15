---
UID: NF:wincrypt.CertGetValidUsages
title: CertGetValidUsages function
author: windows-sdk-content
description: Returns an array of usages that consist of the intersection of the valid usages for all certificates in an array of certificates.
old-location: security\certgetvalidusages.htm
tech.root: seccrypto
ms.assetid: 1504f166-2fa9-4041-9d72-b150cd8baa8a
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CertGetValidUsages, CertGetValidUsages function [Security], _crypto2_certgetvalidusages, security.certgetvalidusages, wincrypt/CertGetValidUsages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetValidUsages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertGetValidUsages function


## -description


The <b>CertGetValidUsages</b> function returns an array of usages that consist of the intersection of the valid usages for all certificates in an array of certificates.


## -parameters




### -param cCerts [in]

The number of certificates in the array to be checked.


### -param rghCerts [in]

An array of certificates to be checked for valid usage.


### -param cNumOIDs [out]

The number of valid usages found as the intersection of the valid usages of all certificates in the array. If all of the certificates are valid for all usages, <i>cNumOIDs</i> is set to negative one (–1).


### -param rghOIDs [out]

An array of the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) of the valid usages that are shared by all of the certificates in the <i>rghCerts</i> array. This parameter can be <b>NULL</b> to set the size of this structure for memory allocation purposes. For more information, see 
<a href="https://msdn.microsoft.com/ef99edef-39b2-4d78-9c01-13720215d47f">Retrieving Data of Unknown Length</a>.


### -param pcbOIDs [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the <i>rghOIDs</i> array and the strings pointed to. When the function returns, the <b>DWORD</b> value contains the number of bytes needed for the array.


## -returns



If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



