---
UID: NF:credentialprovider.ICredentialProviderFilter.Filter
title: ICredentialProviderFilter::Filter (credentialprovider.h)
description: Evaluates whether a list of credential providers should be allowed to provide credential tiles.
helpviewer_keywords: ["CREDUIWIN_AUTHPACKAGE_ONLY","CREDUIWIN_CHECKBOX","CREDUIWIN_ENUMERATE_ADMINS","CREDUIWIN_ENUMERATE_CURRENT_USER","CREDUIWIN_GENERIC","CREDUIWIN_IN_CRED_ONLY","CREDUIWIN_PACK_32_WOW","Filter","Filter method [Windows Shell]","Filter method [Windows Shell]","ICredentialProviderFilter interface","ICredentialProviderFilter interface [Windows Shell]","Filter method","ICredentialProviderFilter.Filter","ICredentialProviderFilter::Filter","_shell_ICredentialProviderFilter_Filter","credentialprovider/ICredentialProviderFilter::Filter","shell.ICredentialProviderFilter_Filter"]
old-location: shell\ICredentialProviderFilter_Filter.htm
tech.root: shell
ms.assetid: 3ba60965-6f18-427f-851d-b92c71eb03d2
ms.date: 12/05/2018
ms.keywords: CREDUIWIN_AUTHPACKAGE_ONLY, CREDUIWIN_CHECKBOX, CREDUIWIN_ENUMERATE_ADMINS, CREDUIWIN_ENUMERATE_CURRENT_USER, CREDUIWIN_GENERIC, CREDUIWIN_IN_CRED_ONLY, CREDUIWIN_PACK_32_WOW, Filter, Filter method [Windows Shell], Filter method [Windows Shell],ICredentialProviderFilter interface, ICredentialProviderFilter interface [Windows Shell],Filter method, ICredentialProviderFilter.Filter, ICredentialProviderFilter::Filter, _shell_ICredentialProviderFilter_Filter, credentialprovider/ICredentialProviderFilter::Filter, shell.ICredentialProviderFilter_Filter
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderFilter::Filter
 - credentialprovider/ICredentialProviderFilter::Filter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Credentialprovider.h
api_name:
 - ICredentialProviderFilter.Filter
---

# ICredentialProviderFilter::Filter


## -description

Evaluates whether a list of credential providers should be allowed to provide credential tiles.

## -parameters

### -param cpus [in]

Type: <b><a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a></b>

A pointer to a <a href="/windows/win32/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario">CREDENTIAL_PROVIDER_USAGE_SCENARIO</a> value that declares the scenarios in which a credential provider is supported.

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

