---
UID: NF:setupapi.SetupGetFieldCount
title: SetupGetFieldCount function
author: windows-driver-content
description: The SetupGetFieldCount function retrieves the number of fields in the specified line in an INF file.
old-location: setup\setupgetfieldcount.htm
old-project: SetupApi
ms.assetid: 7353d52c-7553-4f50-beab-7fcc4db1fe40
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SetupGetFieldCount, SetupGetFieldCount function [Setup API], _setupapi_setupgetfieldcount, setup.setupgetfieldcount, setupapi/SetupGetFieldCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Setupapi.dll
-	Ext-MS-Win-SetupAPI-Inf-L1-1-1.dll
api_name:
-	SetupGetFieldCount
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# SetupGetFieldCount function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupGetFieldCount</b> function retrieves the number of fields in the specified line in an INF file.


## -parameters




### -param Context [in]

Pointer to the context for a line in an INF file.


## -returns



This function returns the number of fields on the line. If <i>Context</i> is invalid, 0 is returned. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/08c98745-ecbd-47b4-9d73-2d6765285bae">SetupGetLineCount</a>
 

 

