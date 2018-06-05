---
UID: NF:commctrl.MAKEIPADDRESS
title: MAKEIPADDRESS macro
author: windows-sdk-content
description: Packs four byte-values into a single LPARAM suitable for use with the IPM_SETADDRESS message.
old-location: controls\MAKEIPADDRESS.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\ipaddress\macros\makeipaddress.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: MAKEIPADDRESS, MAKEIPADDRESS macro [Windows Controls], _win32_MAKEIPADDRESS, _win32_MAKEIPADDRESS_cpp, commctrl/MAKEIPADDRESS, controls.MAKEIPADDRESS, controls._win32_MAKEIPADDRESS
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	MAKEIPADDRESS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MAKEIPADDRESS macro


## -description


Packs four byte-values into a single LPARAM suitable for use with the <a href="https://msdn.microsoft.com/52e72437-3558-4789-844f-5ab5b0b7967c">IPM_SETADDRESS</a> message. 


## -parameters




### -param b1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The field 1 address. 


### -param b2

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The field 2 address. 


### -param b3

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The field 3 address. 


### -param b4

TBD






#### - b0

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The field 0 address. 

