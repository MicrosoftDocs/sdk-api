---
UID: NF:authz.AuthzSetAppContainerInformation
title: AuthzSetAppContainerInformation function (authz.h)
description: Sets the app container and capability information in a current Authz context.
helpviewer_keywords: ["AuthzSetAppContainerInformation","AuthzSetAppContainerInformation function [Security]","authz/AuthzSetAppContainerInformation","security.authzsetappcontainerinformation"]
old-location: security\authzsetappcontainerinformation.htm
tech.root: security
ms.assetid: CD01C5E1-2367-4CC1-A495-A295E3C82B46
ms.date: 12/05/2018
ms.keywords: AuthzSetAppContainerInformation, AuthzSetAppContainerInformation function [Security], authz/AuthzSetAppContainerInformation, security.authzsetappcontainerinformation
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuthzSetAppContainerInformation
 - authz/AuthzSetAppContainerInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzSetAppContainerInformation
---

# AuthzSetAppContainerInformation function


## -description

The <b>AuthzSetAppContainerInformation</b> function sets the  app container and capability information in a current Authz context. If the passed in context already has an app container <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) set or if the passed in context is not a valid app container SID, this function fails.

## -parameters

### -param hAuthzClientContext [in]

	The handle to the client context to which the given app container SID and capability SIDs will be added.

### -param pAppContainerSid [in]

The app container SID.

### -param CapabilityCount [in]

The number of capability SIDs to be added. This value can be zero if no capability is to be added.

### -param pCapabilitySids [in, optional]

The capability SIDs to be added to the context. This value must be <b>NULL</b> when the <i>CapabilityCount</i> parameter is zero.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.