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

# ICredentialProviderFilter::Filter


## -description


Evaluates whether a list of credential providers should be allowed to provide credential tiles.


## -parameters




### -param cpus [in]

Type: <b><a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a></b>

A pointer to a <a href="https://msdn.microsoft.com/86025d1d-b13d-4f61-824a-fd471e449567">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> value that declares the scenarios in which a credential provider is supported.


### -param dwFlags [in]

Type: <b>DWORD</b>

Usage scenario flags. This parameter is valid only if <i>cpus</i> is CPUS_CREDUI. They are defined in Wincred.h.





#### CREDUIWIN_GENERIC

Plain text username/password is being requested.



#### CREDUIWIN_CHECKBOX

Show the <b>Save Credential</b> checkbox.



#### CREDUIWIN_AUTHPACKAGE_ONLY

Only credential providers that support the input authentication package should enumerate.



#### CREDUIWIN_IN_CRED_ONLY

Only the incoming credential for the specific authentication package should be enumerated.



#### CREDUIWIN_ENUMERATE_ADMINS

Credential providers should enumerate administrators.



#### CREDUIWIN_ENUMERATE_CURRENT_USER

Only the incoming credential 



#### CREDUIWIN_PACK_32_WOW


### -param rgclsidProviders [in]

Type: <b>GUID*</b>

A pointer to an array of credential provider CLSIDs.


### -param rgbAllow [in, out]

Type: <b>BOOL*</b>

On entry, a pointer to an array of <b>BOOL</b> values, one for each corresponding member of the <i>rgclsidProviders</i> array, all initialized to <b>TRUE</b>. 

                    

On exit, contains <b>TRUE</b> if the corresponding credential provider in <i>rgclsidProviders</i> is allowed to provide a credential tile; otherwise, <b>FALSE</b>.


### -param cProviders [in]

Type: <b>DWORD</b>

The number of members in <i>rgbAllow</i> or <i>rgclsidProviders</i> (they should be the same).


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.




## -remarks



On entry, this method receives two parallel arrays; <i>rgclsidProviders</i>, which contains the credential provider CLSIDs and <i>rgbAllow</i>, which contains <b>BOOL</b> values for the corresponding CLSIDs. <b>ICredentialProviderFilter::Filter</b> looks at each credential provider in <i>rgclsidProviders</i> and decides whether the credential provider should be allowed to enumerate credential tiles for the scenario specified by <i>dwFlags</i>. If this is acceptable, the corresponding entry in <i>rgbAllow</i> is set to <b>TRUE</b>. If this is unacceptable, it is set to <b>FALSE</b>.

Never filter out a CLSID for a credential provider that you do not know about.

Do not filter if <i>cpus</i> is CPUS_CREDUI and a <i>dwFlags</i> value of CREDUIWIN_GENERIC is passed in.

It is legitimate to return success from the method and not modify <i>rgbAllow</i>.



