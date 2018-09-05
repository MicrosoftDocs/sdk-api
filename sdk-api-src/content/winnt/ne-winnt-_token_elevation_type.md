---
UID: NE:winnt._TOKEN_ELEVATION_TYPE
title: "_TOKEN_ELEVATION_TYPE"
author: windows-sdk-content
description: Indicates the elevation type of token being queried by the GetTokenInformation function or set by the SetTokenInformation function.
old-location: security\token_elevation_type_.htm
old-project: SecAuthZ
ms.assetid: bfdfa7b3-a8a9-4e54-896c-4be97521a079
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PTOKEN_ELEVATION_TYPE, PTOKEN_ELEVATION_TYPE, PTOKEN_ELEVATION_TYPE enumeration pointer [Security], TOKEN_ELEVATION_TYPE, TOKEN_ELEVATION_TYPE enumeration [Security], TokenElevationTypeDefault, TokenElevationTypeFull, TokenElevationTypeLimited, _TOKEN_ELEVATION_TYPE, security.token_elevation_type_, winnt/PTOKEN_ELEVATION_TYPE, winnt/TOKEN_ELEVATION_TYPE, winnt/TokenElevationTypeDefault, winnt/TokenElevationTypeFull, winnt/TokenElevationTypeLimited"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TOKEN_ELEVATION_TYPE, *PTOKEN_ELEVATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_ELEVATION_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _TOKEN_ELEVATION_TYPE enumeration


## -description


The <b>TOKEN_ELEVATION_TYPE</b> enumeration indicates the elevation type of token being queried by the <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>  function.


## -enum-fields




### -field TokenElevationTypeDefault

The token does not have a linked token.


### -field TokenElevationTypeFull

The token is an elevated token.


### -field TokenElevationTypeLimited

The token is a limited token.

