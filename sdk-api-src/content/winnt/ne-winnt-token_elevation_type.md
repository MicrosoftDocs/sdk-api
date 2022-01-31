---
UID: NE:winnt._TOKEN_ELEVATION_TYPE
title: TOKEN_ELEVATION_TYPE (winnt.h)
description: Indicates the elevation type of token being queried by the GetTokenInformation function or set by the SetTokenInformation function.
helpviewer_keywords: ["*PTOKEN_ELEVATION_TYPE","PTOKEN_ELEVATION_TYPE","PTOKEN_ELEVATION_TYPE enumeration pointer [Security]","TOKEN_ELEVATION_TYPE","TOKEN_ELEVATION_TYPE enumeration [Security]","TokenElevationTypeDefault","TokenElevationTypeFull","TokenElevationTypeLimited","security.token_elevation_type_","winnt/PTOKEN_ELEVATION_TYPE","winnt/TOKEN_ELEVATION_TYPE","winnt/TokenElevationTypeDefault","winnt/TokenElevationTypeFull","winnt/TokenElevationTypeLimited"]
old-location: security\token_elevation_type_.htm
tech.root: security
ms.assetid: bfdfa7b3-a8a9-4e54-896c-4be97521a079
ms.date: 12/05/2018
ms.keywords: '*PTOKEN_ELEVATION_TYPE, PTOKEN_ELEVATION_TYPE, PTOKEN_ELEVATION_TYPE enumeration pointer [Security], TOKEN_ELEVATION_TYPE, TOKEN_ELEVATION_TYPE enumeration [Security], TokenElevationTypeDefault, TokenElevationTypeFull, TokenElevationTypeLimited, security.token_elevation_type_, winnt/PTOKEN_ELEVATION_TYPE, winnt/TOKEN_ELEVATION_TYPE, winnt/TokenElevationTypeDefault, winnt/TokenElevationTypeFull, winnt/TokenElevationTypeLimited'
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
targetos: Windows
req.typenames: TOKEN_ELEVATION_TYPE, *PTOKEN_ELEVATION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TOKEN_ELEVATION_TYPE
 - winnt/_TOKEN_ELEVATION_TYPE
 - PTOKEN_ELEVATION_TYPE
 - winnt/PTOKEN_ELEVATION_TYPE
 - TOKEN_ELEVATION_TYPE
 - winnt/TOKEN_ELEVATION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_ELEVATION_TYPE
---

# TOKEN_ELEVATION_TYPE enumeration


## -description

The <b>TOKEN_ELEVATION_TYPE</b> enumeration indicates the elevation type of token being queried by the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>  function.

## -enum-fields

### -field TokenElevationTypeDefault:1

The token does not have a linked token.

### -field TokenElevationTypeFull

The token is an elevated token.

### -field TokenElevationTypeLimited

The token is a limited token.
