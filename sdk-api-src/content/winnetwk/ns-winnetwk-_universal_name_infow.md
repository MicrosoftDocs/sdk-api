---
UID: NS:winnetwk._UNIVERSAL_NAME_INFOW
title: "_UNIVERSAL_NAME_INFOW"
author: windows-sdk-content
description: The UNIVERSAL_NAME_INFO structure contains information about the UNC form of a universal name. It is used by the NPGetUniversalName function.
old-location: security\universal_name_info.htm
tech.root: secauthn
ms.assetid: 505bcd3e-4043-4856-9a6f-a6f074dc6076
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*LPUNIVERSAL_NAME_INFOW, LPUNIVERSAL_NAME_INFO, LPUNIVERSAL_NAME_INFO structure pointer [Security], UNIVERSAL_NAME_INFO, UNIVERSAL_NAME_INFO structure [Security], UNIVERSAL_NAME_INFOA, UNIVERSAL_NAME_INFOW, _UNIVERSAL_NAME_INFOW, _mnp_universal_name_info, security.universal_name_info, winnetwk/LPUNIVERSAL_NAME_INFO, winnetwk/UNIVERSAL_NAME_INFO, winnetwk/UNIVERSAL_NAME_INFOA, winnetwk/UNIVERSAL_NAME_INFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UNIVERSAL_NAME_INFOW (Unicode) and UNIVERSAL_NAME_INFOA (ANSI)
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
 - Winnetwk.h
api_name:
 - UNIVERSAL_NAME_INFO
 - UNIVERSAL_NAME_INFOA
 - UNIVERSAL_NAME_INFOW
product: Windows
targetos: Windows
req.typenames: UNIVERSAL_NAME_INFOW, *LPUNIVERSAL_NAME_INFOW
req.redist: 
---

# _UNIVERSAL_NAME_INFOW structure


## -description


The <b>UNIVERSAL_NAME_INFO</b> structure contains information about the UNC form of a universal name. It is used by the 
<a href="https://msdn.microsoft.com/976b5910-c34f-49fa-b25e-82bf607e33a9">NPGetUniversalName</a> function.


## -struct-fields




### -field lpUniversalName

If the provider supports a universal name, it will return that here.

