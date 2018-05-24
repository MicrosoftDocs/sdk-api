---
UID: NF:shlwapi.SHGlobalCounterDecrement
title: SHGlobalCounterDecrement function
author: windows-driver-content
description: Decrements a global counter.
old-location: shell\SHGlobalCounterDecrement.htm
old-project: shell
ms.assetid: 67b45cb9-9d8d-48ef-a7bc-9cd8824bdf2b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: SHGlobalCounterDecrement, SHGlobalCounterDecrement function [Windows Shell], _shell_SHGlobalCounterDecrement, shell.SHGlobalCounterDecrement, shlwapi/SHGlobalCounterDecrement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
api_name:
-	SHGlobalCounterDecrement
product: Windows
targetos: Windows
req.lib: 
req.dll: Shlwapi.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SHGlobalCounterDecrement function


## -description


Decrements a global counter.


## -parameters




### -param id [in]

Type: <b>const <a href="https://msdn.microsoft.com/e96f40fb-3a95-41d2-a45f-a8d91fb544d3">SHGLOBALCOUNTER</a></b>

The <a href="https://msdn.microsoft.com/e96f40fb-3a95-41d2-a45f-a8d91fb544d3">SHGLOBALCOUNTER</a> to decrement.


## -returns



Type: <b>long</b>

The value of the counter after the decrement.




## -see-also




<a href="https://msdn.microsoft.com/e96f40fb-3a95-41d2-a45f-a8d91fb544d3">SHGLOBALCOUNTER</a>



<a href="https://msdn.microsoft.com/cf158770-c9af-4488-9ed0-486e9a528a65">SHGlobalCounterGetValue</a>



<a href="https://msdn.microsoft.com/088efa01-b070-4384-b17a-311aefb0737c">SHGlobalCounterIncrement</a>
 

 

