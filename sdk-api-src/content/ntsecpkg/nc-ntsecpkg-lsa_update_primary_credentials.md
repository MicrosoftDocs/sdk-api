---
UID: NC:ntsecpkg.LSA_UPDATE_PRIMARY_CREDENTIALS
title: LSA_UPDATE_PRIMARY_CREDENTIALS (ntsecpkg.h)
author: windows-sdk-content
description: Provides a mechanism for one security package to notify other packages that the credentials for a logon session have changed.
old-location: security\updatecredentials.htm
tech.root: SecAuthN
ms.assetid: 952ed682-775a-4370-8a89-15ca35553667
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LSA_UPDATE_PRIMARY_CREDENTIALS, LSA_UPDATE_PRIMARY_CREDENTIALS callback, UpdateCredentials, UpdateCredentials callback function [Security], _ssp_updatecredentials, ntsecpkg/UpdateCredentials, security.updatecredentials
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
 - UpdateCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LSA_UPDATE_PRIMARY_CREDENTIALS callback function


## -description


Provides a mechanism for one <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to notify other packages that the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> for a logon <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session</a> have changed.


## -parameters




### -param PrimaryCredentials [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e51fd400-6c3c-4861-ab5c-6c1800b12d31">SECPKG_PRIMARY_CRED</a> structure containing the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary credentials</a>.


### -param Credentials [in, optional]

Optional. Pointer to a 
<a href="https://msdn.microsoft.com/b9514e26-29a5-4ba8-a375-1723c0a1ce39">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">supplemental credentials</a>.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.




## -remarks



To notify packages about the changed credentials, the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) calls the 
<a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a> function implementation in each package.

A pointer to the <b>UpdateCredentials</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/e51fd400-6c3c-4861-ab5c-6c1800b12d31">SECPKG_PRIMARY_CRED</a>



<a href="https://msdn.microsoft.com/b9514e26-29a5-4ba8-a375-1723c0a1ce39">SECPKG_SUPPLEMENTAL_CRED_ARRAY</a>



<a href="https://msdn.microsoft.com/bb382937-e5d6-452b-b166-505d0c80412c">SpAcceptCredentials</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

