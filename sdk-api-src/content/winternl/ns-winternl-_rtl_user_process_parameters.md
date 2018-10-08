---
UID: NS:winternl._RTL_USER_PROCESS_PARAMETERS
title: "_RTL_USER_PROCESS_PARAMETERS"
author: windows-sdk-content
description: Contains process parameter information.
old-location: base\rtl_user_process_parameters.htm
tech.root: procthread
ms.assetid: e736aefa-9945-4526-84d8-adb6e82b9991
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: "*PRTL_USER_PROCESS_PARAMETERS, PRTL_USER_PROCESS_PARAMETERS, PRTL_USER_PROCESS_PARAMETERS structure pointer, RTL_USER_PROCESS_PARAMETERS, RTL_USER_PROCESS_PARAMETERS structure, _RTL_USER_PROCESS_PARAMETERS, base.rtl_user_process_parameters, winternl/PRTL_USER_PROCESS_PARAMETERS, winternl/RTL_USER_PROCESS_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winternl.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - RTL_USER_PROCESS_PARAMETERS
product: Windows
targetos: Windows
req.typenames: RTL_USER_PROCESS_PARAMETERS, *PRTL_USER_PROCESS_PARAMETERS
req.redist: 
---

# _RTL_USER_PROCESS_PARAMETERS structure


## -description


<p class="CCE_Message">[This structure may be altered in future versions of Windows.]

Contains process parameter information.


## -struct-fields




### -field Reserved1

Reserved for internal use by the operating system.


### -field Reserved2

Reserved for internal use by the operating system.


### -field ImagePathName

The path of the image file for the process.


### -field CommandLine

The command-line string passed to the process.


## -see-also




<a href="https://msdn.microsoft.com/836a6b82-d3e8-4de6-808d-5476dfb51356">PEB</a>
 

 

