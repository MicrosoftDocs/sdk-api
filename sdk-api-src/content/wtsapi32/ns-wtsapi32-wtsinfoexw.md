---
UID: NS:wtsapi32._WTSINFOEXW
title: WTSINFOEXW (wtsapi32.h)
description: Contains a WTSINFOEX_LEVEL union that contains extended information about a Remote Desktop Services session. (Unicode)
helpviewer_keywords: ["*PWTSINFOEXW","PWTSINFOEX","PWTSINFOEX structure pointer [Remote Desktop Services]","WTSINFOEX","WTSINFOEX structure [Remote Desktop Services]","WTSINFOEXA","WTSINFOEXW","termserv.wtsinfoex","wtsapi32/PWTSINFOEX","wtsapi32/WTSINFOEX","wtsapi32/WTSINFOEXA","wtsapi32/WTSINFOEXW"]
old-location: termserv\wtsinfoex.htm
tech.root: TermServ
ms.assetid: 94aa2db0-d7e3-4ff2-bff0-d80983d2e8b2
ms.date: 12/05/2018
ms.keywords: '*PWTSINFOEXW, PWTSINFOEX, PWTSINFOEX structure pointer [Remote Desktop Services], WTSINFOEX, WTSINFOEX structure [Remote Desktop Services], WTSINFOEXA, WTSINFOEXW, termserv.wtsinfoex, wtsapi32/PWTSINFOEX, wtsapi32/WTSINFOEX, wtsapi32/WTSINFOEXA, wtsapi32/WTSINFOEXW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSINFOEXW (Unicode) and WTSINFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSINFOEXW, *PWTSINFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTSINFOEXW
 - wtsapi32/_WTSINFOEXW
 - PWTSINFOEXW
 - wtsapi32/PWTSINFOEXW
 - WTSINFOEXW
 - wtsapi32/WTSINFOEXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTSINFOEX
 - WTSINFOEXA
 - WTSINFOEXW
---

# WTSINFOEXW structure


## -description

Contains a <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a> union that contains extended information about a Remote Desktop Services session. This structure is returned by the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function when you specify "WTSSessionInfoEx" for the <i>WTSInfoClass</i> parameter.

## -struct-fields

### -field Level

Specifies the level  of information contained in the <b>Data</b> member. This can be the following value.



#### 1

The <b>Data</b> member is a <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level1_a">WTSINFOEX_LEVEL1</a> structure.

### -field Data

A <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a> union. The type of structure contained here is specified by the <b>Level</b> member.


##### - Level.1

The <b>Data</b> member is a <a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level1_a">WTSINFOEX_LEVEL1</a> structure.

## -see-also

<a href="/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTSINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
