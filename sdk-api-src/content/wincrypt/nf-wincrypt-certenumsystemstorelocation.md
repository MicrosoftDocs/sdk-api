---
UID: NF:wincrypt.CertEnumSystemStoreLocation
title: CertEnumSystemStoreLocation function
author: windows-sdk-content
description: The CertEnumSystemStoreLocation function retrieves all of the system store locations. The function calls the provided callback function for each system store location found.
old-location: security\certenumsystemstorelocation.htm
tech.root: seccrypto
ms.assetid: 86408e6f-0732-4cb4-85cd-840b9d98b973
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CertEnumSystemStoreLocation, CertEnumSystemStoreLocation function [Security], _crypto2_certenumsystemstorelocation, security.certenumsystemstorelocation, wincrypt/CertEnumSystemStoreLocation
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
 - CertEnumSystemStoreLocation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertEnumSystemStoreLocation function


## -description


The <b>CertEnumSystemStoreLocation</b> function retrieves all of the system store locations. The function calls the provided callback function for each system store location found.


## -parameters




### -param dwFlags [in]

Reserved for future use; must be zero.


### -param pvArg [in]

A pointer to a <b>void</b>  that allows the application to declare, define, and initialize a structure to hold any information to be passed to the callback enumeration function.


### -param pfnEnum [in]

A pointer to the callback function used to show the details for each store location. This callback function determines the content and format for the presentation of information on each store location. For the signature and parameters of the callback function, see <a href="https://msdn.microsoft.com/a5f1badd-3e68-4e0f-9a42-1b1876c9cb56">CertEnumSystemStoreLocationCallback</a>.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.
						
						

If the function fails, it returns <b>FALSE</b>.




## -remarks



To use <b>CertEnumSystemStoreLocation</b>, an application must declare and define the <b>ENUM_ARG</b> structure and an enumeration callback function.


#### Examples

For an example that uses this function, see 
<a href="https://msdn.microsoft.com/bc4268ea-f657-4789-9d0a-6e5354508f86">Example C Program: Listing System and Physical Stores</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/5804d565-5129-4e6d-8b3d-9bd938807740">CertEnumPhysicalStore</a>



<a href="https://msdn.microsoft.com/fd9cb23b-e4a3-41cb-8f0a-30f4e813c6ac">CertEnumSystemStore</a>



<a href="https://msdn.microsoft.com/e301c76d-cacd-441a-b925-754b07e4bfa9">CertRegisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/b6f72826-92ab-4e21-8db9-eb053663148b">CertRegisterSystemStore</a>



<a href="https://msdn.microsoft.com/06480a2f-5a94-4cf5-9774-ceb9499e1d44">CertUnregisterPhysicalStore</a>



<a href="https://msdn.microsoft.com/958e4185-4c37-450c-abfc-91b95593227e">CertUnregisterSystemStore</a>



<a href="cryptography_functions.htm">Certificate Store Functions</a>
 

 

