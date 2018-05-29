---
UID: NF:setupapi.SetupIterateCabinetW
title: SetupIterateCabinetW function
author: windows-sdk-content
description: The SetupIterateCabinet function iterates through all the files in a cabinet and sends a notification to a callback function for each file found.
old-location: setup\setupiteratecabinet.htm
old-project: SetupApi
ms.assetid: 2fa2d140-fa8e-41a8-9800-d10e5559fab4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: SetupIterateCabinet, SetupIterateCabinet function [Setup API], SetupIterateCabinetA, SetupIterateCabinetW, _setupapi_setupiteratecabinet, setup.setupiteratecabinet, setupapi/SetupIterateCabinet, setupapi/SetupIterateCabinetA, setupapi/SetupIterateCabinetW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupIterateCabinetW (Unicode) and SetupIterateCabinetA (ANSI)
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
-	Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
-	Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
-	SetupIterateCabinet
-	SetupIterateCabinetA
-	SetupIterateCabinetW
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SetupIterateCabinetW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupIterateCabinet</b> function iterates through all the files in a cabinet and sends a notification to a callback function for each file found.


## -parameters




### -param CabinetFile [in]

Cabinet (.CAB) file to iterate through.


### -param Reserved [in]

Not currently used.


### -param MsgHandler [in]

Pointer to a <a href="https://msdn.microsoft.com/41eaa57a-e116-443c-93ee-397456a5c466">FileCallback</a> routine that will process the notifications 
<b>SetupIterateCabinet</b> returns as it iterates through the files in the cabinet file. The callback routine may then return a value specifying whether to decompress, copy, or skip the file.


### -param Context [in]

Context value that is passed into the routine specified in <i>MsgHandler</i>. This enables the callback routine to track values between notifications, without having to use global variables.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

