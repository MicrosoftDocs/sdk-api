---
UID: NS:wtsapi32._WTSINFOEXA
title: WTSINFOEXA (wtsapi32.h)
description: Contains a WTSINFOEX_LEVEL union that contains extended information about a Remote Desktop Services session.helpviewer_keywords: ["*PWTSINFOEXA","PWTSINFOEX","PWTSINFOEX structure pointer [Remote Desktop Services]","WTSINFOEX","WTSINFOEX structure [Remote Desktop Services]","WTSINFOEXA","WTSINFOEXW","termserv.wtsinfoex","wtsapi32/PWTSINFOEX","wtsapi32/WTSINFOEX","wtsapi32/WTSINFOEXA","wtsapi32/WTSINFOEXW"]
old-location: termserv\wtsinfoex.htm
tech.root: TermServ
ms.assetid: 94aa2db0-d7e3-4ff2-bff0-d80983d2e8b2
ms.date: 12/05/2018
ms.keywords: '*PWTSINFOEXA, PWTSINFOEX, PWTSINFOEX structure pointer [Remote Desktop Services], WTSINFOEX, WTSINFOEX structure [Remote Desktop Services], WTSINFOEXA, WTSINFOEXW, termserv.wtsinfoex, wtsapi32/PWTSINFOEX, wtsapi32/WTSINFOEX, wtsapi32/WTSINFOEXA, wtsapi32/WTSINFOEXW'
f1_keywords:
- wtsapi32/WTSINFOEX
dev_langs:
- c++
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
targetos: Windows
req.typenames: WTSINFOEXA, *PWTSINFOEXA
req.redist: 
ms.custom: 19H1
---

# WTSINFOEXA structure


## -description


Contains a <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a> union that contains extended information about a Remote Desktop Services session. This structure is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function when you specify "WTSSessionInfoEx" for the <i>WTSInfoClass</i> parameter.


## -struct-fields




### -field Level

Specifies the level  of information contained in the <b>Data</b> member. This can be the following value.



#### 1

The <b>Data</b> member is a <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level1_a">WTSINFOEX_LEVEL1</a> structure.


### -field Data

A <a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a> union. The type of structure contained here is specified by the <b>Level</b> member.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/ns-wtsapi32-wtsinfoex_level_a">WTSINFOEX_LEVEL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>
 

 

