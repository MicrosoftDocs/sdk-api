---
UID: NS:schannel._SecPkgContext_SessionAppData
title: SecPkgContext_SessionAppData
author: windows-sdk-content
description: Stores application data for a session context.
old-location: security\secpkgcontext_sessionappdata.htm
tech.root: secauthn
ms.assetid: 7bda791a-dd60-4651-bfe8-13333017d6a3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSecPkgContext_SessionAppData, SecPkgContext_SessionAppData, SecPkgContext_SessionAppData structure [Security], schannel/SecPkgContext_SessionAppData, security.secpkgcontext_sessionappdata"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: schannel.h
req.include-header: Schnlsp.h
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
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SecPkgContext_SessionAppData
product: Windows
targetos: Windows
req.typenames: SecPkgContext_SessionAppData, *PSecPkgContext_SessionAppData
req.redist: 
---

# SecPkgContext_SessionAppData structure


## -description


The <b>SecPkgContext_SessionAppData</b> structure stores application data for a session context.

This attribute is supported only by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).


## -struct-fields




### -field dwFlags

Reserved for future use.


### -field cbAppData

Count of bytes used by <b>pbAppData</b>.


### -field pbAppData

Pointer to a <b>BYTE</b> that represents the session application data.

