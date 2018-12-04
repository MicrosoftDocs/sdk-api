---
UID: NF:ntmsapi.GetNtmsObjectInformationW
title: GetNtmsObjectInformationW function
author: windows-sdk-content
description: The GetNtmsObjectInformation function returns an object's information structure for the specified object.
old-location: fs\getntmsobjectinformation.htm
tech.root: Rsm
ms.assetid: e5c1b165-2c55-40c3-94d8-c996c5db4250
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetNtmsObjectInformation, GetNtmsObjectInformation function [Files], GetNtmsObjectInformationA, GetNtmsObjectInformationW, _zaw_getntmsobjectinformation, base.getntmsobjectinformation, fs.getntmsobjectinformation, ntmsapi/GetNtmsObjectInformation, ntmsapi/GetNtmsObjectInformationA, ntmsapi/GetNtmsObjectInformationW
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
req.unicode-ansi: GetNtmsObjectInformationW (Unicode) and GetNtmsObjectInformationA (ANSI)
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
 - GetNtmsObjectInformation
 - GetNtmsObjectInformationA
 - GetNtmsObjectInformationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNtmsObjectInformationW function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsObjectInformation</b> function returns an object's information structure for the specified object.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpObjectId [in]

Unique identifier of the RSM object.


### -param lpInfo [out]

Pointer to an 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure that receives the object information.


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
 NTMS_USE_ACCESS to the object or its container is denied. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>No access rights are required.

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
The object ID or information structure is missing, or the object information size or object type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An allocation failure occurred during processing.

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



The information size and type of the information structure must be set correctly in the <i>lpInfo</i> parameter before you use the 
<b>GetNtmsObjectInformation</b> function.

To avoid unpredictable results, applications must call the 
<b>GetNtmsObjectInformation</b> function before calling the 
<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a> function. The 
<b>SetNtmsObjectInformation</b> function updates all writable members of the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure, therefore the application is responsible for providing a value for all writable members.

The following is the list of objects that require special access rights.

<table>
<tr>
<th>Object</th>
<th>Access</th>
</tr>
<tr>
<td>NTMS_CHANGER</td>
<td>Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_CHANGER_TYPE</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_COMPUTER</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_DRIVE</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_DRIVE_TYPE</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_IEDOOR</td>
<td>Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_IEPORT</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LIBRARY</td>
<td> Requires NTMS_USE_ACCESS to the library.
						</td>
</tr>
<tr>
<td>NTMS_LIBREQUEST</td>
<td> Requires NTMS_USE_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LOGICAL_MEDIA</td>
<td>Requires NTMS_USE_ACCESS to the media pool of the logical media.
						</td>
</tr>
<tr>
<td>NTMS_MEDIA_TYPE</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_OPREQUEST</td>
<td> Requires NTMS_USE_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_PARTITION</td>
<td> Requires NTMS_USE_ACCESS to the media pool of the side.
						</td>
</tr>
<tr>
<td>NTMS_PHYSICAL_MEDIA</td>
<td> Requires NTMS_USE_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_STORAGESLOT</td>
<td>Requires NTMS_USE_ACCESS to the library.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d2168a3-077e-48fc-8a06-91952213f2cb">GetNtmsObjectSecurity</a>



<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>



<a href="removable_storage_manager_functions.htm">Object Management Functions</a>



<a href="https://msdn.microsoft.com/1cdb9c72-1b34-4800-a07d-b648baec8582">SetNtmsObjectInformation</a>
 

 

