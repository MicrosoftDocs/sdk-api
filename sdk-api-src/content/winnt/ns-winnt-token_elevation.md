---
UID: NS:winnt._TOKEN_ELEVATION
title: TOKEN_ELEVATION (winnt.h)
author: windows-sdk-content
description: Indicates whether a token has elevated privileges.
old-location: security\token_elevation.htm
tech.root: SecAuthZ
ms.assetid: a1c87818-f092-43cf-872d-4bb2590a944b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTOKEN_ELEVATION, PTOKEN_ELEVATION, PTOKEN_ELEVATION structure pointer [Security], TOKEN_ELEVATION, TOKEN_ELEVATION structure [Security], _TOKEN_ELEVATION, security.token_elevation, winnt/PTOKEN_ELEVATION, winnt/TOKEN_ELEVATION"
ms.topic: struct
f1_keywords: 
 - "winnt/TOKEN_ELEVATION"
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Winnt.h
api_name:
 - TOKEN_ELEVATION
product: Windows
targetos: Windows
req.typenames: TOKEN_ELEVATION, *PTOKEN_ELEVATION
req.redist: 
ms.custom: 19H1
---

# TOKEN_ELEVATION structure


## -description


The <b>TOKEN_ELEVATION</b> structure indicates whether a token has elevated privileges.


## -struct-fields




### -field TokenIsElevated

A nonzero value if the token has elevated privileges; otherwise, a zero value.

