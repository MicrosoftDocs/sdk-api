---
UID: NF:azroles.IAzNameResolver.NameFromSid
title: IAzNameResolver::NameFromSid
author: windows-sdk-content
description: Gets the display name that corresponds to the specified security identifier (SID).
old-location: security\iaznameresolver_namefromsid_method.htm
old-project: secauthz
ms.assetid: 3518e620-85cf-4bae-8366-d43564535774
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: IAzNameResolver interface [Security],NameFromSid method, IAzNameResolver.NameFromSid, IAzNameResolver::NameFromSid, NameFromSid, NameFromSid method [Security], NameFromSid method [Security],IAzNameResolver interface, azroles/IAzNameResolver::NameFromSid, security.iaznameresolver_namefromsid_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzNameResolver.NameFromSid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzNameResolver::NameFromSid


## -description


The <b>NameFromSid</b> method gets the display name that corresponds to the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -parameters




### -param bstrSid [in]

The string representation of the SID to translate.


### -param pSidType [out]

An element of the <a href="https://msdn.microsoft.com/4e6af6bd-056b-4f5a-b223-57a673c3fcfa">SID_NAME_USE</a> enumeration that specifies the type of SID being translated.


### -param pbstrName [out]

A pointer to the display name of the principal that corresponds to the SID specified by the <i>bstrSid</i> parameter.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. In particular, if the method cannot find the display name of the principal, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



