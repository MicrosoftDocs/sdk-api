---
UID: NS:wsman._WSMAN_SHELL_STARTUP_INFO_V11
title: WSMAN_SHELL_STARTUP_INFO_V11 (wsman.h)
description: The WSMAN_SHELL_STARTUP_INFO_V11 (wsman.h) structure defines the shell startup parameters to be used with the WSManCreateShell function.
helpviewer_keywords: ["WSMAN_SHELL_STARTUP_INFO","WSMAN_SHELL_STARTUP_INFO structure [Windows Remote Management]","WSMAN_SHELL_STARTUP_INFO_V11","winrm.wsman_shell_startup_info","wsman/WSMAN_SHELL_STARTUP_INFO"]
old-location: winrm\wsman_shell_startup_info.htm
tech.root: winrm
ms.assetid: a9e004de-b157-4ad3-a463-a42ccb56f1ba
ms.date: 08/16/2022
ms.keywords: WSMAN_SHELL_STARTUP_INFO, WSMAN_SHELL_STARTUP_INFO structure [Windows Remote Management], WSMAN_SHELL_STARTUP_INFO_V11, winrm.wsman_shell_startup_info, wsman/WSMAN_SHELL_STARTUP_INFO
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: WSMAN_SHELL_STARTUP_INFO_V11
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_SHELL_STARTUP_INFO_V11
 - wsman/_WSMAN_SHELL_STARTUP_INFO_V11
 - WSMAN_SHELL_STARTUP_INFO_V11
 - wsman/WSMAN_SHELL_STARTUP_INFO_V11
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_STARTUP_INFO
---

# WSMAN_SHELL_STARTUP_INFO_V11 structure


## -description

Defines the shell startup parameters to be used with the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> function. The structure must be allocated by the client and passed to the <b>WSManCreateShell</b> function. 

The configuration passed to the <a href="/windows/desktop/api/wsman/nf-wsman-wsmancreateshell">WSManCreateShell</a> function can directly affect the behavior of a command executed within the shell. A typical example is the <i>workingDirectory</i> argument that describes the working directory associated with each process, which the operating system uses when attempting to locate files specified by using a relative path. 

In the absence of specific requirements for stream naming, clients and services should attempt to use <b>STDIN</b> for input streams, <b>STDOUT</b> for the default output stream, and <b>STDERR</b> for the error or status output stream.

## -struct-fields

### -field name

Specifies an optional friendly name to be associated with the shell. This parameter is only functional when the client passes the  flag <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> to WSManInitialize.

### -field _WSMAN_SHELL_STARTUP_INFO_V10

 




#### - idleTimeoutMs

Specifies the maximum duration, in milliseconds, the shell will stay open without any client request. When the maximum duration is exceeded, the shell is automatically deleted. Any value from 0  to 0xFFFFFFFF can be set. This duration has a maximum value specified by the Idle time-out GPO setting, if enabled, or by the IdleTimeout local configuration. The default value of the maximum duration in the GPO/local configuration is 15 minutes. However, a system administrator can change this value. To use the maximum value from the GPO/local configuration, the client should specify 0 (zero) in this field. If an explicit value between 0 to 0xFFFFFFFF is used, the minimum value between the explicit API value and the value from the GPO/local configuration is used.


#### - inputStreamSet

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_stream_id_set">WSMAN_STREAM_ID_SET</a> structure that specifies a set of input streams for the shell. Streams not present in the filter can be ignored by the shell implementation.  For the Windows Cmd.exe shell, this value should be L"stdin".
If the value is <b>NULL</b>, the implementation uses an array with L"stdin" as the default value.


#### - outputStreamSet

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_stream_id_set">WSMAN_STREAM_ID_SET</a> structure that specifies a set of output streams for the shell.  Streams not present in the filter can be ignored by the shell implementation. For the Windows cmd.exe shell, this value should be L"stdout stderr".
If the value is <b>NULL</b>, the implementation uses an array with L"stdout" and L"stderr" as the default value.


#### - variableSet

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_environment_variable_set">WSMAN_ENVIRONMENT_VARIABLE_SET</a> structure that specifies an array of variable name and value pairs, which describe the starting environment for the shell. The content of these elements is shell specific and can be defined in terms of other environment variables. If a <b>NULL</b> value is passed, the default environment is used on the server side.


#### - workingDirectory

Specifies the starting directory for a shell. It is  used with any execution command. If this member is a <b>NULL</b> value, a default directory will be used by the remote machine when executing the command. An empty value is treated by the underlying protocol as an omitted value.
