---
UID: NS:setupapi._SP_REGISTER_CONTROL_STATUSW
title: SP_REGISTER_CONTROL_STATUSW (setupapi.h)
author: windows-sdk-content
description: The SP_REGISTER_CONTROL_STATUS structure contains information about a file being registered or unregistered using the RegisterDlls INF directive to self-register DLLs on Windows 2000.
old-location: setup\sp_register_control_status.htm
tech.root: SetupApi
ms.assetid: aeeedba8-f788-4f95-9583-e76dbb116db9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSP_REGISTER_CONTROL_STATUSW, PSP_REGISTER_CONTROL_STATUS, PSP_REGISTER_CONTROL_STATUS structure pointer [Setup API], SPREG_DLLINSTALL, SPREG_GETPROCADDR, SPREG_LOADLIBRARY, SPREG_REGSVR, SPREG_SUCCESS, SPREG_TIMEOUT, SPREG_UNKNOWN, SP_REGISTER_CONTROL_STATUS, SP_REGISTER_CONTROL_STATUS structure [Setup API], SP_REGISTER_CONTROL_STATUSW, _setupapi_sp_register_control_status, setup.sp_register_control_status, setupapi/PSP_REGISTER_CONTROL_STATUS, setupapi/SP_REGISTER_CONTROL_STATUS"
ms.topic: struct
f1_keywords: ["setupapi/SP_REGISTER_CONTROL_STATUS"]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_REGISTER_CONTROL_STATUS
product: Windows
targetos: Windows
req.typenames: SP_REGISTER_CONTROL_STATUSW, *PSP_REGISTER_CONTROL_STATUSW
req.redist: 
ms.custom: 19H1
---

# SP_REGISTER_CONTROL_STATUSW structure


## -description


The 
<b>SP_REGISTER_CONTROL_STATUS</b> structure contains information about a file being registered or unregistered using the <b>RegisterDlls </b>INF directive to self-register DLLs on Windows 2000.

When 
<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a> sends a 
<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-startregistration">SPFILENOTIFY_STARTREGISTRATION</a> or 
<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-endregistration">SPFILENOTIFY_ENDREGISTRATION</a> notification to the callback routine, the caller must provide a pointer to a <b>SP_REGISTER_CONTROL_STATUS</b> structure in the <i>MsgHandler</i> parameter.


## -struct-fields




### -field cbSize

 


### -field FileName

Fully qualified path of the file being registered or unregistered.


### -field Win32Error

For an SPFILENOTIFY_STARTREGISTRATION notification, this member is not used and should be set to NO_ERROR. For a SPFILENOTIFY_ENDREGISTRATION notification, set to a <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>.


### -field FailureCode

For a SPFILENOTIFY_STARTREGISTRATION notification, this member is not used and should be set to SPREG_SUCCESS. For a SPFILENOTIFY_ENDREGISTRATION notification, set to one of the following failure codes that indicate the result of registration. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPREG_SUCCESS"></a><a id="spreg_success"></a><dl>
<dt><b>SPREG_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The file was successfully registered or unregistered. <b>WinError</b> not used.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_LOADLIBRARY"></a><a id="spreg_loadlibrary"></a><dl>
<dt><b>SPREG_LOADLIBRARY</b></dt>
</dl>
</td>
<td width="60%">
<b>LoadLibrary</b> failed for the file. <b>WinError</b> contains an extended error code from the component.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_GETPROCADDR"></a><a id="spreg_getprocaddr"></a><dl>
<dt><b>SPREG_GETPROCADDR</b></dt>
</dl>
</td>
<td width="60%">
<b>GetProcAddress</b> failed for the file. <b>WinError</b> contains an extended error code from the component.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_REGSVR"></a><a id="spreg_regsvr"></a><dl>
<dt><b>SPREG_REGSVR</b></dt>
</dl>
</td>
<td width="60%">
<b>DLLRegisterServer</b> entry point returned failure. <b>WinError</b> contains an extended error code from the component.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_DLLINSTALL"></a><a id="spreg_dllinstall"></a><dl>
<dt><b>SPREG_DLLINSTALL</b></dt>
</dl>
</td>
<td width="60%">
<b>DLLInstall</b> entry point returned failure. <b>WinError</b> contains an extended error code from the component.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_TIMEOUT"></a><a id="spreg_timeout"></a><dl>
<dt><b>SPREG_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The file registration or unregistration exceeded the specified timeout. <b>WinError</b> is set to ERROR_TIMEOUT.

</td>
</tr>
<tr>
<td width="40%"><a id="SPREG_UNKNOWN"></a><a id="spreg_unknown"></a><dl>
<dt><b>SPREG_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
File registration or unregistration failed for an unknown reason. <b>WinError</b> indicates an extended error code from the component.

</td>
</tr>
</table>
 


#### - cbsize

Size of the structure, in bytes.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SetupApi/overview">Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-endregistration">SPFILENOTIFY_ENDREGISTRATION</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/spfilenotify-startregistration">SPFILENOTIFY_STARTREGISTRATION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupinstallfrominfsectiona">SetupInstallFromInfSection</a>



<a href="https://docs.microsoft.com/windows/desktop/SetupApi/structures--setup-api-">Structures</a>
 

 

