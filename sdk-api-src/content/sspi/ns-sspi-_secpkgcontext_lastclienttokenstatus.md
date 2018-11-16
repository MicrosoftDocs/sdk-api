---
UID: NS:sspi._SecPkgContext_LastClientTokenStatus
title: "_SecPkgContext_LastClientTokenStatus"
author: windows-sdk-content
description: Specifies whether the token from the most recent call to the InitializeSecurityContext function is the last token from the client.
old-location: security\secpkgcontext_lastclienttokenstatus.htm
tech.root: SecAuthN
ms.assetid: ccb2bb4e-3c65-4305-95ad-b9111f3936b5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PSecPkgContext_LastClientTokenStatus, PSecPkgContext_LastClientTokenStatus, PSecPkgContext_LastClientTokenStatus structure pointer [Security], SecPkgContext_LastClientTokenStatus, SecPkgContext_LastClientTokenStatus structure [Security], _SecPkgContext_LastClientTokenStatus, security.secpkgcontext_lastclienttokenstatus, sspi/PSecPkgContext_LastClientTokenStatus, sspi/SecPkgContext_LastClientTokenStatus"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: sspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_LastClientTokenStatus
product: Windows
targetos: Windows
req.typenames: SecPkgContext_LastClientTokenStatus, *PSecPkgContext_LastClientTokenStatus
req.redist: 
---

# _SecPkgContext_LastClientTokenStatus structure


## -description


Specifies whether the token from the most recent call to the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a> function is the last token from the client.


## -struct-fields




### -field LastClientTokenStatus

A value of the <a href="https://msdn.microsoft.com/b9067862-2339-4543-a8cd-610e6f921bfd">SECPKG_ATTR_LCT_STATUS</a> enumeration that indicates the status of the token returned by the most recent  call to <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext</a>.


## -see-also




<a href="https://msdn.microsoft.com/b9067862-2339-4543-a8cd-610e6f921bfd">SECPKG_ATTR_LCT_STATUS</a>
 

 

