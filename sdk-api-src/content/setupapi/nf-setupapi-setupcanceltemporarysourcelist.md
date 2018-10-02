---
UID: NF:setupapi.SetupCancelTemporarySourceList
title: SetupCancelTemporarySourceList function
author: windows-sdk-content
description: The SetupCancelTemporarySourceList function cancels any temporary list and no-browse behavior and reestablishes standard list behavior.
old-location: setup\setupcanceltemporarysourcelist.htm
tech.root: SetupApi
ms.assetid: 87ef9425-5dab-442b-a487-3a4789005411
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupCancelTemporarySourceList, SetupCancelTemporarySourceList function [Setup API], _setupapi_setupcanceltemporarysourcelist, setup.setupcanceltemporarysourcelist, setupapi/SetupCancelTemporarySourceList
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
 - SetupCancelTemporarySourceList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetupCancelTemporarySourceList function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupCancelTemporarySourceList</b> function cancels any temporary list and no-browse behavior and reestablishes standard list behavior.


## -parameters






## -returns



If a temporary list was in effect, the return value is a nonzero value. Otherwise, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6a37a56c-ae44-4a57-9307-90efcf025d1a">SetupSetSourceList</a>
 

 

