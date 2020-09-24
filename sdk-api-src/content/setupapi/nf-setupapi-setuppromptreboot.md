---
UID: NF:setupapi.SetupPromptReboot
title: SetupPromptReboot function (setupapi.h)
description: The SetupPromptReboot function asks the user if he wants to reboot the system, optionally dependent on whether any files in a committed file queue were in use during a file operation.
helpviewer_keywords: ["SetupPromptReboot","SetupPromptReboot function [Setup API]","_setupapi_setuppromptreboot","setup.setuppromptreboot","setupapi/SetupPromptReboot"]
old-location: setup\setuppromptreboot.htm
tech.root: setup
ms.assetid: 14b34fd9-ae96-4552-b99d-488bae5c7644
ms.date: 12/05/2018
ms.keywords: SetupPromptReboot, SetupPromptReboot function [Setup API], _setupapi_setuppromptreboot, setup.setuppromptreboot, setupapi/SetupPromptReboot
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupPromptReboot
 - setupapi/SetupPromptReboot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
api_name:
 - SetupPromptReboot
---

# SetupPromptReboot function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupPromptReboot</b> function asks the user if he wants to reboot the system, optionally dependent on whether any files in a committed file queue were in use during a file operation. If the user answers "yes" to the prompt, shutdown is initiated before this routine returns.

## -parameters

### -param FileQueue [in]

Optional pointer to a handle to the file queue upon which to base the decision about whether shutdown is necessary. If <i>FileQueue</i> is not specified, 
<b>SetupPromptReboot</b> assumes shutdown is necessary and asks the user what to do.

### -param Owner [in]

Handle for the parent window to own windows created by this function.

### -param ScanOnly [in]

Indicates whether or not to prompt the user when 
<b>SetupPromptReboot</b> is called. 




If <b>TRUE</b>, the user is never asked about rebooting, and system shutdown is not initiated. In this case, <i>FileQueue</i> must be specified. If <b>FALSE</b>, the user is asked about rebooting, as previously described.

Use <i>ScanOnly</i> to determine if shutdown is necessary separately from actually initiating a shutdown.

## -returns

The function returns a combination of the following flags or –1 if an error occurs.

To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setuppromptfordiska">SetupPromptForDisk</a>