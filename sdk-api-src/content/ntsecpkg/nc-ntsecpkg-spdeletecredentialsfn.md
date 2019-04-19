---
UID: NC:ntsecpkg.SpDeleteCredentialsFn
title: SpDeleteCredentialsFn (ntsecpkg.h)
author: windows-sdk-content
description: Deletes credentials from a security package's list of primary or supplemental credentials.
old-location: security\spdeletecredentials.htm
tech.root: SecAuthN
ms.assetid: 14f41fc2-1e28-4ae5-9f2e-00f2500b7819
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpDeleteCredentials, SpDeleteCredentials callback function [Security], SpDeleteCredentialsFn, SpDeleteCredentialsFn callback, _ssp_spdeletecredentials, ntsecpkg/SpDeleteCredentials, security.spdeletecredentials
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
 - SpDeleteCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpDeleteCredentialsFn callback function


## -description


Deletes <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> from a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package's</a> list of <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> or <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental</a> credentials.


## -parameters




### -param CredentialHandle [in]

A handle to the credentials to delete.


### -param Key [in]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure whose contents indicate which credentials to delete. The information stored in the <i>Key</i> parameter is package specific.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpDeleteCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpDeleteCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

