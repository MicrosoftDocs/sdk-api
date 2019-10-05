---
UID: NC:ntsecpkg.SpSaveCredentialsFn
title: SpSaveCredentialsFn (ntsecpkg.h)
author: windows-sdk-content
description: Saves a supplemental credential to the user object.
old-location: security\spsavecredentials.htm
tech.root: SecAuthN
ms.assetid: 15983acb-6fa3-4c53-9ede-a41db95c82f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SpSaveCredentials, SpSaveCredentials callback function [Security], SpSaveCredentialsFn, SpSaveCredentialsFn callback, _ssp_spsavecredentials, ntsecpkg/SpSaveCredentials, security.spsavecredentials
ms.topic: callback
f1_keywords:
- ntsecpkg/SpSaveCredentials
dev_langs:
 - c++
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
- SpSaveCredentials
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpSaveCredentialsFn callback function


## -description


Saves a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">supplemental credential</a> to the user object.


## -parameters




### -param CredentialHandle [in]

A handle to the credential to save.


### -param Credentials [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure containing the credential information to be saved.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



SSP/APs must implement the <b>SpSaveCredentials</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpSaveCredentials</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spmarshallsupplementalcredsfn">SpMarshallSupplementalCreds</a>
 

 

