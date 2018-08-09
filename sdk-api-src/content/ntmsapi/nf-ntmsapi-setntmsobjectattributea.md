---
UID: NF:ntmsapi.SetNtmsObjectAttributeA
title: SetNtmsObjectAttributeA function
author: windows-sdk-content
description: The SetNtmsObjectAttribute function creates an extended attribute (named private data) in the specified RSM object.
old-location: fs\setntmsobjectattribute.htm
old-project: Rsm
ms.assetid: ce572b2a-f4c3-4cf3-8bb3-074ba3d1ec30
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: SetNtmsObjectAttribute, SetNtmsObjectAttribute function [Files], SetNtmsObjectAttributeA, SetNtmsObjectAttributeW, _zaw_setntmsobjectattribute, base.setntmsobjectattribute, fs.setntmsobjectattribute, ntmsapi/SetNtmsObjectAttribute, ntmsapi/SetNtmsObjectAttributeA, ntmsapi/SetNtmsObjectAttributeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetNtmsObjectAttributeW (Unicode) and SetNtmsObjectAttributeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - SetNtmsObjectAttribute
 - SetNtmsObjectAttributeA
 - SetNtmsObjectAttributeW
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# SetNtmsObjectAttributeA function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsObjectAttribute</b> function creates an extended attribute (named private data) in the specified RSM object.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpObjectId [in]

GUID of the RSM object for which the extended attribute is to be created.


### -param dwType [in]

RSM object type. For a list of object types, see 
<a href="https://msdn.microsoft.com/598e7cb1-f463-4252-9bdf-ccb98f36f4da">NtmsObjectsTypes</a>.


### -param lpAttributeName [in]

Name of the extended attribute to be created.


### -param lpAttributeData [in]

User-defined data.


### -param dwAttributeSize

TBD




#### - AttributeSize [in]

Size of the <i>lpAttributeData</i> buffer, in bytes.


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
 NTMS_MODIFY_ACCESS is denied to the object or no modifications are allowed for the specified object type (see Remarks). Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>No access rights are required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name or attribute is not valid. The NTMS_MAXATTR_NAMELEN value defines the maximum attribute name length. The length includes a <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The pointer is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
The attribute specified is greater than or equal to NTMS_MAXATTR_LENGTH.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The GUID is not valid.

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



The 
<b>SetNtmsObjectAttribute</b> function must be executed on the specified RSM server. Because the buffer of bytes is unmarshaled between systems of different architectures, remote execution of this function can result in unpredictable results.

To delete an attribute, perform a set of the attribute with a length of zero.

The following is the list of objects that require special access rights.

<table>
<tr>
<th>Object</th>
<th>Access</th>
</tr>
<tr>
<td>NTMS_CHANGER</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_CHANGER_TYPE</td>
<td>Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_COMPUTER</td>
<td>Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_DRIVE</td>
<td>Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_DRIVE_TYPE</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_IEDOOR</td>
<td>Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_IEPORT</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LIBRARY</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.
						</td>
</tr>
<tr>
<td>NTMS_LIBREQUEST</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
<tr>
<td>NTMS_LOGICAL_MEDIA</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool of the logical media.
						</td>
</tr>
<tr>
<td>NTMS_MEDIA_POOL</td>
<td>Requires NTMS_MODIFY_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_MEDIA_TYPE</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_OPREQUEST</td>
<td> Requires NTMS_MODIFY_ACCESS to the computer.</td>
</tr>
<tr>
<td>NTMS_PARTITION</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool of the side.
						</td>
</tr>
<tr>
<td>NTMS_PHYSICAL_MEDIA</td>
<td> Requires NTMS_MODIFY_ACCESS to the media pool.</td>
</tr>
<tr>
<td>NTMS_STORAGESLOT</td>
<td> Requires NTMS_MODIFY_ACCESS to the library.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a>



<a href="https://msdn.microsoft.com/9a92d60c-a25f-4775-adb9-1a02af3c8917">GetNtmsObjectAttribute</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Object Management Functions</a>
 

 

