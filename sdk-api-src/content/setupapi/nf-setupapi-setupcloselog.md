---
UID: NF:setupapi.SetupCloseLog
title: SetupCloseLog function
author: windows-sdk-content
description: The SetupCloseLog function closes the log files.
old-location: setup\setupcloselog.htm
tech.root: SetupApi
ms.assetid: 659e7922-205c-4da2-90ed-aa7d7625af87
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetupCloseLog, SetupCloseLog function [Setup API], _setupapi_setupcloselog, setup.setupcloselog, setupapi/SetupCloseLog
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
 - Ext-MS-Win-setupapi-logging-l1-1-0.dll
api_name:
 - SetupCloseLog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetupCloseLog
: 
---

# SetupCloseLog function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The <b>SetupCloseLog</b> function closes the log files.


## -parameters






## -returns



This function does not return a value.




## -remarks



The log files are located in the Windows directory, and the file names are Setupact.log and Setuperr.log.




## -see-also




<a href="https://msdn.microsoft.com/0a9518b7-f231-48f2-ba50-5b802f8ccaed">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

