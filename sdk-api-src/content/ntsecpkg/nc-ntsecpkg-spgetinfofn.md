---
UID: NC:ntsecpkg.SpGetInfoFn
title: SpGetInfoFn
author: windows-sdk-content
description: Provides general information about the security package, such as its name and capabilities.
old-location: security\spgetinfo.htm
old-project: SecAuthN
ms.assetid: e1e6f71f-6f54-424c-be49-7bc11cb19036
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SpGetInfo, SpGetInfo function [Security], SpGetInfoFn, _ssp_spgetinfo, ntsecpkg/SpGetInfo, security.spgetinfo
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
-	SpGetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpGetInfoFn callback function


## -description


The <b>SpGetInfo</b> function provides general information about the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>, such as its name and capabilities.

The <b>SpGetInfo</b> function is called when the client calls the 
<a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param PackageInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure that is allocated by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) and must be populated by the package.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



It is safe to place pointers to constant or dynamic data into the 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure—the LSA will make a copy of the data prior to forwarding it.

SSP/APs must implement the <b>SpGetInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetInfo</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

