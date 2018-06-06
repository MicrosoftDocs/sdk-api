---
UID: NS:wtsapi32._WTSINFOEXA
title: "_WTSINFOEXA"
author: windows-sdk-content
description: Contains a WTSINFOEX_LEVEL union that contains extended information about a Remote Desktop Services session.
old-location: termserv\wtsinfoex.htm
old-project: TermServ
ms.assetid: 94aa2db0-d7e3-4ff2-bff0-d80983d2e8b2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PWTSINFOEXA, PWTSINFOEX, PWTSINFOEX structure pointer [Remote Desktop Services], WTSINFOEX, WTSINFOEX structure [Remote Desktop Services], WTSINFOEXA, WTSINFOEXW, _WTSINFOEXA, termserv.wtsinfoex, wtsapi32/PWTSINFOEX, wtsapi32/WTSINFOEX, wtsapi32/WTSINFOEXA, wtsapi32/WTSINFOEXW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WTSINFOEXA, *PWTSINFOEXA
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WTSINFOEXA structure


## -description


Contains a <a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a> union that contains extended information about a Remote Desktop Services session. This structure is returned by the <a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a> function when you specify "WTSSessionInfoEx" for the <i>WTSInfoClass</i> parameter.


## -struct-fields




### -field Level

Specifies the level  of information contained in the <b>Data</b> member. This can be the following value.



#### 1

The <b>Data</b> member is a <a href="https://msdn.microsoft.com/bad4f35a-04a9-42fa-b87e-0f51e9f0f30e">WTSINFOEX_LEVEL1</a> structure.


### -field Data

A <a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a> union. The type of structure contained here is specified by the <b>Level</b> member.


## -see-also




<a href="https://msdn.microsoft.com/d3df1f40-698b-43ca-808d-0df5550b6eae">WTSINFOEX_LEVEL</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

