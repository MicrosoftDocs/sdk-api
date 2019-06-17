---
UID: NF:commctrl.MAKEIPADDRESS
title: MAKEIPADDRESS macro (commctrl.h)
author: windows-sdk-content
description: Packs four byte-values into a single LPARAM suitable for use with the IPM_SETADDRESS message.
old-location: controls\MAKEIPADDRESS.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeipaddress.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MAKEIPADDRESS, MAKEIPADDRESS macro [Windows Controls], _win32_MAKEIPADDRESS, _win32_MAKEIPADDRESS_cpp, commctrl/MAKEIPADDRESS, controls.MAKEIPADDRESS, controls._win32_MAKEIPADDRESS
ms.topic: macro
f1_keywords: ["commctrl/MAKEIPADDRESS"]
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
 - MAKEIPADDRESS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MAKEIPADDRESS macro


## -description


Packs four byte-values into a single LPARAM suitable for use with the <a href="https://docs.microsoft.com/windows/desktop/Controls/ipm-setaddress">IPM_SETADDRESS</a> message. 


## -parameters




### -param b1

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 0 address. 


### -param b2

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 1 address. 


### -param b3

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 2 address. 


### -param b4

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The field 3 address. 

