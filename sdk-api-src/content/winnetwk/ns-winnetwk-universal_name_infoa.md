---
UID: NS:winnetwk._UNIVERSAL_NAME_INFOA
title: UNIVERSAL_NAME_INFOA (winnetwk.h)
description: The UNIVERSAL_NAME_INFO structure contains information about the UNC form of a universal name. It is used by the NPGetUniversalName function.helpviewer_keywords: ["*LPUNIVERSAL_NAME_INFOA","LPUNIVERSAL_NAME_INFO","LPUNIVERSAL_NAME_INFO structure pointer [Security]","UNIVERSAL_NAME_INFO","UNIVERSAL_NAME_INFO structure [Security]","UNIVERSAL_NAME_INFOA","UNIVERSAL_NAME_INFOW","_mnp_universal_name_info","security.universal_name_info","winnetwk/LPUNIVERSAL_NAME_INFO","winnetwk/UNIVERSAL_NAME_INFO","winnetwk/UNIVERSAL_NAME_INFOA","winnetwk/UNIVERSAL_NAME_INFOW"]
old-location: security\universal_name_info.htm
tech.root: SecAuthN
ms.assetid: 505bcd3e-4043-4856-9a6f-a6f074dc6076
ms.date: 12/05/2018
ms.keywords: '*LPUNIVERSAL_NAME_INFOA, LPUNIVERSAL_NAME_INFO, LPUNIVERSAL_NAME_INFO structure pointer [Security], UNIVERSAL_NAME_INFO, UNIVERSAL_NAME_INFO structure [Security], UNIVERSAL_NAME_INFOA, UNIVERSAL_NAME_INFOW, _mnp_universal_name_info, security.universal_name_info, winnetwk/LPUNIVERSAL_NAME_INFO, winnetwk/UNIVERSAL_NAME_INFO, winnetwk/UNIVERSAL_NAME_INFOA, winnetwk/UNIVERSAL_NAME_INFOW'
f1_keywords:
- winnetwk/UNIVERSAL_NAME_INFO
dev_langs:
- c++
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
targetos: Windows
req.typenames: UNIVERSAL_NAME_INFOA, *LPUNIVERSAL_NAME_INFOA
req.redist: 
ms.custom: 19H1
---

# UNIVERSAL_NAME_INFOA structure


## -description


The <b>UNIVERSAL_NAME_INFO</b> structure contains information about the UNC form of a universal name. It is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/npapi/nf-npapi-npgetuniversalname">NPGetUniversalName</a> function.


## -struct-fields




### -field lpUniversalName

If the provider supports a universal name, it will return that here.

