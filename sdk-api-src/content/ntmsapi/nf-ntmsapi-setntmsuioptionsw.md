---
UID: NF:ntmsapi.SetNtmsUIOptionsW
title: SetNtmsUIOptionsW function (ntmsapi.h)
description: The SetNtmsUIOptions function modifies the list of computer names to which the specified type of UI is being directed for the given object. (Unicode)
helpviewer_keywords: ["NTMS_UIDEST_ADD", "NTMS_UIDEST_DELETE", "NTMS_UIDEST_DELETEALL", "NTMS_UITYPE_ERR", "NTMS_UITYPE_INFO", "NTMS_UITYPE_REQ", "SetNtmsUIOptions", "SetNtmsUIOptions function [Files]", "SetNtmsUIOptionsW", "_zaw_setntmsuioptions", "base.setntmsuioptions", "fs.setntmsuioptions", "ntmsapi/SetNtmsUIOptions", "ntmsapi/SetNtmsUIOptionsW"]
old-location: fs\setntmsuioptions.htm
tech.root: fs
ms.assetid: 1e76fddc-20b4-4645-9519-2033487dbbc5
ms.date: 12/05/2018
ms.keywords: NTMS_UIDEST_ADD, NTMS_UIDEST_DELETE, NTMS_UIDEST_DELETEALL, NTMS_UITYPE_ERR, NTMS_UITYPE_INFO, NTMS_UITYPE_REQ, SetNtmsUIOptions, SetNtmsUIOptions function [Files], SetNtmsUIOptionsA, SetNtmsUIOptionsW, _zaw_setntmsuioptions, base.setntmsuioptions, fs.setntmsuioptions, ntmsapi/SetNtmsUIOptions, ntmsapi/SetNtmsUIOptionsA, ntmsapi/SetNtmsUIOptionsW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetNtmsUIOptionsW (Unicode) and SetNtmsUIOptionsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetNtmsUIOptionsW
 - ntmsapi/SetNtmsUIOptionsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - SetNtmsUIOptions
 - SetNtmsUIOptionsA
 - SetNtmsUIOptionsW
---

# SetNtmsUIOptionsW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SetNtmsUIOptions</b> function modifies the list of computer names to which the specified type of UI is being directed for the given object.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the object whose UI is being redirected. The object must be a container that can be a source for events. The object can be either be an application (a mount request triggered by the application), a library (a door open request in response to an eject) or a computer (all UI pertaining to the computer). 




To specify the computer container set the <i>lpObjectId</i> pointer to point to a buffer with the Removable Storage Manager's computer object GUID. To specify a particular library set it to point to a buffer with the library's GUID. To specify an application, pass in a <b>NULL</b> pointer. The identity of the application is determined by the session used in <i>hSession</i>. Note that an application can have multiple sessions open simultaneously. In this case, the value set applies only to the <i>hSession</i> session. In the case of a library or computer instance, settings persist until explicitly changed. Application rows are deleted when the session is closed.

### -param dwType [in]

This parameter can have one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_UITYPE_INFO"></a><a id="ntms_uitype_info"></a><dl>
<dt><b>NTMS_UITYPE_INFO</b></dt>
</dl>
</td>
<td width="60%">
UI messages that provide information. These include the work queue items that indicate progress. For example, mount requests.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_UITYPE_REQ"></a><a id="ntms_uitype_req"></a><dl>
<dt><b>NTMS_UITYPE_REQ</b></dt>
</dl>
</td>
<td width="60%">
UI messages that are requests. These include the operator requests that handle media. For example, a request to inject new media.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_UITYPE_ERR"></a><a id="ntms_uitype_err"></a><dl>
<dt><b>NTMS_UITYPE_ERR</b></dt>
</dl>
</td>
<td width="60%">
UI messages that give error information. These include operator requests that are related to error notification. For example, a request to clean the drive.

</td>
</tr>
</table>

### -param dwOperation [in]

This parameter can have one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_UIDEST_ADD"></a><a id="ntms_uidest_add"></a><dl>
<dt><b>NTMS_UIDEST_ADD</b></dt>
</dl>
</td>
<td width="60%">
Add a new destination (computer name) to the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_UIDEST_DELETE"></a><a id="ntms_uidest_delete"></a><dl>
<dt><b>NTMS_UIDEST_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Remove a destination from the list.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_UIDEST_DELETEALL"></a><a id="ntms_uidest_deleteall"></a><dl>
<dt><b>NTMS_UIDEST_DELETEALL</b></dt>
</dl>
</td>
<td width="60%">
Clear all destinations from the list. No UI for the object is generated. In this case, the destination argument is ignored.

</td>
</tr>
</table>

### -param lpszDestination [out]

Multi-string that returns the names of the computers to which the UI is being redirected. This parameter cannot be <b>NULL</b>.

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
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The given destination already exists in the list.

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
<i>lpdwSize</i> or <i>lpszDestination</i> pointer is <b>NULL</b>, or <i>lpObjectId</i> is not a valid container, or <i>dwType</i> or <i>dwOperation</i> is not one of the three valid values.

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
The GUID specified by <i>lpObjectId</i> is not the GUID of any computer or library object in the database.

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

A call to 
<b>SetNtmsUIOptions</b> adds or removes a destination for a particular instance determined by the <i>lpObjectId</i> and <i>dwType</i> parameters.

<table>
<tr>
<th> </th>
<th>NTMS_UITYPE_INFO</th>
<th>NTMS_UITYPE_REQ</th>
<th>NTMS_UITYPE_ERR</th>
</tr>
<tr>
<td>Application</td>
<td>Display work item progress UI for work items generated by this application.</td>
<td>Display operator request UI for operator requests generated by actions taken by this application.</td>
<td>Undefined. Applications cannot cause this sort of error event.</td>
</tr>
<tr>
<td>Library</td>
<td>Display work item progress UI for work items associated with this library.</td>
<td>Display UI for requests associated with this library.</td>
<td>Display UI for errors associated with this library.</td>
</tr>
<tr>
<td>Computer</td>
<td>Display informational UI in this instance of RSM running on this machine.</td>
<td>Display a request-type UI in this instance of RSM.</td>
<td>Display error-type UI in this instance of RSM.</td>
</tr>
</table>
 

Note that security checks are performed when calling 
<b>SetNtmsUIOptions</b>. When the computer object is specified you are required to have access with permission to modify the computer. When modifying a library's UI element you are required to have access with permission to modify the library object.

Note that there is no checking of destination strings. A call to with a destination name that's not a computer reachable from the computer on which 
<b>SetNtmsUIOptions</b> called returns success. A pointer to an empty string is taken to mean the local machine.





> [!NOTE]
> The ntmsapi.h header defines SetNtmsUIOptions as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsuioptionsa">GetNtmsUIOptions</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>
