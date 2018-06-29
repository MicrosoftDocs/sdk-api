---
UID: NF:setupapi.SetupOpenLog
title: SetupOpenLog function
author: windows-sdk-content
description: The SetupOpenLog function opens the log files.
old-location: setup\setupopenlog.htm
old-project: SetupApi
ms.assetid: 3ff13002-7811-4e44-b12b-52d0d4c8de60
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: SetupOpenLog, SetupOpenLog function [Setup API], _setupapi_setupopenlog, setup.setupopenlog, setupapi/SetupOpenLog
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-setupapi-logging-l1-1-0.dll
api_name:
 - SetupOpenLog
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
req.product: ADAM
---

# SetupOpenLog function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The  <b>SetupOpenLog</b> function opens the log files.


## -parameters




### -param Erase

TBD




#### - Reserved [in]

Must be FALSE.


## -returns



<b>TRUE</b> if the log file can be opened. <b>FALSE</b> if an error occurs. To get the  error code, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



 The log files are located in the Windows directory, and the file names are Setupact.log and Setuperr.log.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>
 

 

