---
UID: NF:setupapi.SetupFreeSourceListW
title: SetupFreeSourceListW function
author: windows-sdk-content
description: The SetupFreeSourceList function frees the system resources allocated to a source list.
old-location: setup\setupfreesourcelist.htm
tech.root: SetupApi
ms.assetid: ac326a2c-df67-4a3e-9290-663f84027a48
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupFreeSourceList, SetupFreeSourceList function [Setup API], SetupFreeSourceListA, SetupFreeSourceListW, _setupapi_setupfreesourcelist, setup.setupfreesourcelist, setupapi/SetupFreeSourceList, setupapi/SetupFreeSourceListA, setupapi/SetupFreeSourceListW
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
req.unicode-ansi: SetupFreeSourceListW (Unicode) and SetupFreeSourceListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupFreeSourceList
 - SetupFreeSourceListA
 - SetupFreeSourceListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupFreeSourceListW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupFreeSourceList</b> function frees the system resources allocated to a source list.


## -parameters




### -param List [in, out]

Pointer to an array of sources from 
<a href="https://msdn.microsoft.com/8d1de1d5-5b82-45ae-b29c-4f9a93d28c6e">SetupQuerySourceList</a>. The <b>null</b>-terminated string should not exceed the size of the destination buffer. When the function returns, this pointer is set to <b>NULL</b>.


### -param Count [in]

Number of sources in the list.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/87ef9425-5dab-442b-a487-3a4789005411">SetupCancelTemporarySourceList</a>



<a href="https://msdn.microsoft.com/6a37a56c-ae44-4a57-9307-90efcf025d1a">SetupSetSourceList</a>
 

 

