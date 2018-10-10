---
UID: NF:commctrl.MAKEIPRANGE
title: MAKEIPRANGE macro
author: windows-sdk-content
description: Packs two byte-values into a single LPARAM suitable for use with the IPM_SETRANGE message.
old-location: controls\MAKEIPRANGE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeiprange.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: MAKEIPRANGE, MAKEIPRANGE macro [Windows Controls], _win32_MAKEIPRANGE, _win32_MAKEIPRANGE_cpp, commctrl/MAKEIPRANGE, controls.MAKEIPRANGE, controls._win32_MAKEIPRANGE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - Commctrl.h
api_name:
 - MAKEIPRANGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MAKEIPRANGE macro


## -description


Packs two byte-values into a single LPARAM suitable for use with the <a href="https://msdn.microsoft.com/en-us/library/Bb761382(v=VS.85).aspx">IPM_SETRANGE</a> message. 


## -parameters




### -param low

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BYTE</a></b>

The lower limit of the range. 


### -param high

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BYTE</a></b>

The upper limit of the range. 

