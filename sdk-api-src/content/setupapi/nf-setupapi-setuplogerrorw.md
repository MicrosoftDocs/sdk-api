---
UID: NF:setupapi.SetupLogErrorW
title: SetupLogErrorW function (setupapi.h)

description: The SetupLogError function writes an error message to a log file.
old-location: setup\setuplogerror.htm
tech.root: SetupApi
ms.assetid: 1e003338-9ada-48cb-89cc-557f12a43cd0

ms.date: 12/05/2018
ms.keywords: SetupLogError, SetupLogError function [Setup API], SetupLogErrorA, SetupLogErrorW, _setupapi_setuplogerror, setup.setuplogerror, setupapi/SetupLogError, setupapi/SetupLogErrorA, setupapi/SetupLogErrorW
ms.topic: function
f1_keywords: 
 - "setupapi/SetupLogError"
dev_langs:
 - c++
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupLogErrorW (Unicode) and SetupLogErrorA (ANSI)
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
 - SetupLogError
 - SetupLogErrorA
 - SetupLogErrorW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupLogErrorW function


## -description


<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupLogError</b> function writes an error message to a log file. It is meant to be used during the installation of Windows, but it is always available. It is not intended to be used after the operating system is installed — the event log should be used instead.


## -parameters




### -param MessageString [in]

Pointer to the string that should be saved to Setup's log. The message must end with a return-linefeed combination (\r\n). You should use a null-terminated string. The null-terminated string should not exceed the size of the destination buffer. The message is always saved to the action log, setupact.log. If <i>Severity</i> is <b>LogSevWarning</b>, <b>LogSevError</b>, or <b>LogSevFatalError</b>, Setup also saves the message to the error log, setuperr.log. Both logs are stored in the Windows directory.


### -param Severity [in]

Severity of the message, one of the following: <b>LogSevInformation</b>, <b>LogSevWarning</b>, <b>LogSevError</b>, or <b>LogSevFatalError</b>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



<ul>
<li>The action log is intended for recording all modifications made to the system during installation of Windows.</li>
<li>The error log is intended for errors during installation of Windows only.</li>
<li>The <i>MessageString</i> parameter may be formatted further by Setup (though it does no additional processing now).</li>
<li>The error log will be presented to the user at the end of system  setup.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/functions">Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>
 

 

