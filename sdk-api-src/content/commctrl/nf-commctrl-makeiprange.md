---
UID: NF:commctrl.MAKEIPRANGE
title: MAKEIPRANGE macro
author: windows-sdk-content
description: Packs two byte-values into a single LPARAM suitable for use with the IPM_SETRANGE message.
old-location: controls\MAKEIPRANGE.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeiprange.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MAKEIPRANGE, MAKEIPRANGE macro [Windows Controls], _win32_MAKEIPRANGE, _win32_MAKEIPRANGE_cpp, commctrl/MAKEIPRANGE, controls.MAKEIPRANGE, controls._win32_MAKEIPRANGE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STGOPTIONS
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
req.lib: 
req.dll: 
req.irql: 
---

# MAKEIPRANGE macro


## -description


Packs two byte-values into a single LPARAM suitable for use with the <a href="https://msdn.microsoft.com/en-us/library/Bb761382(v=VS.85).aspx">IPM_SETRANGE</a> message. 


## -parameters




### -param low

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The lower limit of the range. 


### -param high

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The upper limit of the range. 

