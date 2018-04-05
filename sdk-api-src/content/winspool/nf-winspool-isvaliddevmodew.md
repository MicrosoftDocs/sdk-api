---
UID: NF:winspool.IsValidDevmodeW
title: IsValidDevmodeW function
author: windows-driver-content
description: The IsValidDevmode function verifies that the contents of a DEVMODE structure are valid.
old-location: gdi\isvaliddevmode.htm
old-project: printdocs
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IsValidDevmode, IsValidDevmode function [Windows GDI], IsValidDevmodeA, IsValidDevmodeW, _win32_isvaliddevmode, gdi.isvaliddevmode, winspool/IsValidDevmode, winspool/IsValidDevmodeA, winspool/IsValidDevmodeW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winspool.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IsValidDevmodeW (Unicode) and IsValidDevmodeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winspool.drv
api_name:
-	IsValidDevmode
-	IsValidDevmodeA
-	IsValidDevmodeW
product: Windows
targetos: Windows
req.lib: Winspool.lib
req.dll: Winspool.drv
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsValidDevmodeW function


## -description


The <b>IsValidDevmode</b> function verifies that the contents of a DEVMODE 
structure are valid.


## -parameters




### -param pDevmode [in]

A pointer to the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> to validate.


### -param DevmodeSize

The size in bytes of the input byte buffer.


## -returns



<b>TRUE</b>, if the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> is structurally valid. If minor errors are found the function will fix them and return <b>TRUE</b>.

<b>FALSE</b>, if the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> has one or more significant structural problems. For example, its <b>dmSize</b> member is misaligned or specifies a buffer that is too small. Also, <b>FALSE</b> if <b>pDevmode</b> is <b>NULL</b>.




## -remarks



No private printer driver fields of the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> are checked, only the public fields.

Callers should use <b>dmSize</b>+<b>dmDriverExtra</b> for <b>DevmodeSize</b> only if they can guarantee that the input buffer size is at least that big. Since the <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> is generally untrusted data, the values that are in the input buffer at the <b>dmSize</b> and <b>dmDriverExtra</b> offsets are also untrusted.

This function is executable in Least-Privileged User Account (LUA) context.




## -see-also




<a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a>



<a href="https://msdn.microsoft.com/d859f84d-af0e-4b8b-b7fa-d7b1fc35ed39">Print Spooler API Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn614611">Printing</a>
 

 

