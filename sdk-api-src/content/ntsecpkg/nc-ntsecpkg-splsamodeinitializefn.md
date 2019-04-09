---
UID: NC:ntsecpkg.SpLsaModeInitializeFn
title: SpLsaModeInitializeFn (ntsecpkg.h)
author: windows-sdk-content
description: Provides the LSA with pointers to the functions implemented by each security package in the SSP/AP DLL.
old-location: security\splsamodeinitialize.htm
tech.root: SecAuthN
ms.assetid: 1ef3770b-197f-4d5b-9933-b7f6f63e5627
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpLsaModeInitialize, SpLsaModeInitialize callback function [Security], SpLsaModeInitializeFn, SpLsaModeInitializeFn callback, _ssp_splsamodeinitialize, ntsecpkg/SpLsaModeInitialize, security.splsamodeinitialize
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpLsaModeInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SpLsaModeInitializeFn callback function


## -description


The <b>SpLsaModeInitialize</b> function is called once by the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) for each registered <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a>/<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> (SSP/AP) DLL it loads. This function provides the LSA with pointers to the functions implemented by each <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> in the SSP/AP DLL.


## -parameters




### -param LsaVersion [in]

The version of the LSA.


### -param PackageVersion [out]

Pointer to a <b>ULONG</b> that returns the SSP/AP DLL version number.


### -param *ppTables [out]

Pointer to an array of 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structures. Each structure is a table of pointers to the functions implemented by a security package deployed in the SSP/AP DLL.


### -param pcTables [out]

Pointer that returns the number of elements in the array pointed to by the <i>ppTables</i> parameter.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <b>SpLsaModeInitialize</b> function must be implemented by SSP/AP DLLs.

The <i>ppTables</i> parameter should contain one 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> for each security package deployed in the DLL.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>
 

 

