---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SP_REGISTER_CONTROL_STATUSA structure


## -description


The 
<b>SP_REGISTER_CONTROL_STATUS</b> structure contains information about a file being registered or unregistered using the <b>RegisterDlls </b>INF directive to self-register DLLs on Windows 2000.

When 
<a href="https://msdn.microsoft.com/bd1ee91a-b58b-4f08-9181-42fbe9d763f9">SetupInstallFromInfSection</a> sends a 
<a href="https://msdn.microsoft.com/0faf277c-7805-478f-9cec-0dd7b6acdb0e">SPFILENOTIFY_STARTREGISTRATION</a> or 
<a href="https://msdn.microsoft.com/6304f406-c9f8-41cc-a7b7-5ef606f62efb">SPFILENOTIFY_ENDREGISTRATION</a> notification to the callback routine, the caller must provide a pointer to a <b>SP_REGISTER_CONTROL_STATUS</b> structure in the <i>MsgHandler</i> parameter.


## -struct-fields




### -field cbSize

 


### -field FileName

Fully qualified path of the file being registered or unregistered.


### -field Win32Error

For an SPFILENOTIFY_STARTREGISTRATION notification, this member is not used and should be set to NO_ERROR. For a SPFILENOTIFY_ENDREGISTRATION notification, set to a <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.


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




<a href="https://msdn.microsoft.com/58201596-cb8c-480a-abef-896c1f9ef098">Overview</a>



<a href="https://msdn.microsoft.com/6304f406-c9f8-41cc-a7b7-5ef606f62efb">SPFILENOTIFY_ENDREGISTRATION</a>



<a href="https://msdn.microsoft.com/0faf277c-7805-478f-9cec-0dd7b6acdb0e">SPFILENOTIFY_STARTREGISTRATION</a>



<a href="https://msdn.microsoft.com/bd1ee91a-b58b-4f08-9181-42fbe9d763f9">SetupInstallFromInfSection</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

