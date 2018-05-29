---
UID: NC:ntsecpkg.SpGetExtendedInformationFn
title: SpGetExtendedInformationFn
author: windows-sdk-content
description: Provides extended information about a security package.
old-location: security\spgetextendedinformation.htm
old-project: SecAuthN
ms.assetid: e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SpGetExtendedInformation, SpGetExtendedInformation function [Security], SpGetExtendedInformationFn, _ssp_spgetextendedinformation, ntsecpkg/SpGetExtendedInformation, security.spgetextendedinformation
ms.prod: windows
ms.technology: windows-sdk
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
-	SpGetExtendedInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpGetExtendedInformationFn callback function


## -description



			The <b>SpGetExtendedInformation</b> function provides extended information about a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.


## -parameters




### -param Class [in]

A value from the 
<a href="https://msdn.microsoft.com/52c24886-ae81-4ac8-97d5-d638016e82bf">SECPKG_EXTENDED_INFORMATION_CLASS</a> enumeration indicating the type of extended information.


### -param *ppInformation [out]

Pointer to a pointer to a 
<a href="https://msdn.microsoft.com/3d80dfc0-c35b-4d14-8196-02944c3db8d2">SECPKG_EXTENDED_INFORMATION</a> structure allocated by the security package. If the function call succeeds, the returned structure contains the requested information.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



Extended information is set using the 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> function.

An SSP/AP must implement the <b>SpGetExtendedInformation</b> function; however, the actual name given to the implementation is up to the package developer.

A pointer to the <b>SpGetExtendedInformation</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3d80dfc0-c35b-4d14-8196-02944c3db8d2">SECPKG_EXTENDED_INFORMATION</a>



<a href="https://msdn.microsoft.com/52c24886-ae81-4ac8-97d5-d638016e82bf">SECPKG_EXTENDED_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>



<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a>
 

 

