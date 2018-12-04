---
UID: NF:ntmsapi.SetNtmsObjectSecurity
title: SetNtmsObjectSecurity function
author: windows-sdk-content
description: The SetNtmsObjectSecurity function writes the security descriptor for the specified RSM object.
old-location: fs\setntmsobjectsecurity.htm
tech.root: Rsm
ms.assetid: ea6be316-6188-46a2-b12a-fe8426bc5fac
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: SetNtmsObjectSecurity, SetNtmsObjectSecurity function [Files], _zaw_setntmsobjectsecurity, base.setntmsobjectsecurity, fs.setntmsobjectsecurity, ntmsapi/SetNtmsObjectSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntmsapi.h
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - SetNtmsObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetNtmsObjectSecurity function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsObjectSecurity</b> function writes the security descriptor for the specified RSM object.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpObjectId [in]

Unique identifier of the RSM object.


### -param dwType [in]

RSM object type. For a list of object types, see the 
<a href="https://msdn.microsoft.com/598e7cb1-f463-4252-9bdf-ccb98f36f4da">NtmsObjectsTypes</a>.


### -param SecurityInformation [in]

A 
<a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> value that specifies the security information to write to the RSM object.


### -param lpSecurityDescriptor [in]

Pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure that specifies the security descriptor to write to the RSM object: NTMS_USE_ACCESS, NTMS_CONTROL_ACCESS, or NTMS_MODIFY_ACCESS.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The privileges required to modify the security descriptor are denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database is inaccessible or damaged.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The database is full.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is missing or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The object ID is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SECURITY_ON_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
There is no security information for this object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The object ID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>
 




## -remarks



If an application uses 
<b>SetNtmsObjectSecurity</b> to set the discretionary access-control list (ACL) of an object, the application must have WRITE_DAC permission or be the owner of the object.

If an application uses 
<b>SetNtmsObjectSecurity</b> to set the system ACL of an object, the SE_SECURITY_NAME privilege must be enabled for the application. For more information, see the <a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a> function. For more information on RSM security, see 
<a href="https://msdn.microsoft.com/9a0dd513-f8c0-454f-be3a-fbea7c865994">RSM Security</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a>



<a href="https://msdn.microsoft.com/1d2168a3-077e-48fc-8a06-91952213f2cb">GetNtmsObjectSecurity</a>



<a href="removable_storage_manager_functions.htm">Object Management Functions</a>
 

 

