---
UID: NE:winspool.EPrintXPSJobOperation
title: EPrintXPSJobOperation
author: windows-driver-content
description: Specifies whether an XPS print job is in the spooling or the rendering phase.
old-location: gdi\eprintxpsjoboperation.htm
old-project: printdocs
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: EPrintXPSJobOperation, EPrintXPSJobOperation enumeration [Windows GDI], _win32_EPrintXPSJobOperation, gdi.eprintxpsjoboperation, kJobConsumption, kJobProduction, winspool/EPrintXPSJobOperation, winspool/kJobConsumption, winspool/kJobProduction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EPrintXPSJobOperation
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	EPrintXPSJobOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EPrintXPSJobOperation enumeration


## -description


Specifies whether an XPS print job is in the spooling or the rendering phase.


## -enum-fields




### -field kJobProduction

The XPS job is spooling.


### -field kJobConsumption

The XPS job is rendering.


## -remarks



This enumeration is primarily used as a parameter for the <a href="https://msdn.microsoft.com/66f7483d-be98-410d-b0c7-430743397de2">ReportJobProcessingProgress</a> function.



