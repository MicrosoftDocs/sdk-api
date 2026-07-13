---
UID: NF:ntmsapi.GetNtmsUIOptionsW
title: GetNtmsUIOptionsW function (ntmsapi.h)
description: The GetNtmsUIOptions function obtains the list of computer names to which the specified type of user interface is being directed for the given object. (Unicode)
helpviewer_keywords: ["GetNtmsUIOptions", "GetNtmsUIOptions function [Files]", "GetNtmsUIOptionsW", "NTMS_UITYPE_ERR", "NTMS_UITYPE_INFO", "NTMS_UITYPE_REQ", "_zaw_getntmsuioptions", "base.getntmsuioptions", "fs.getntmsuioptions", "ntmsapi/GetNtmsUIOptions", "ntmsapi/GetNtmsUIOptionsW"]
old-location: fs\getntmsuioptions.htm
tech.root: fs
ms.assetid: 69267981-1d68-4af9-ae4b-5d4cb3a18c57
ms.date: 12/05/2018
ms.keywords: GetNtmsUIOptions, GetNtmsUIOptions function [Files], GetNtmsUIOptionsA, GetNtmsUIOptionsW, NTMS_UITYPE_ERR, NTMS_UITYPE_INFO, NTMS_UITYPE_REQ, _zaw_getntmsuioptions, base.getntmsuioptions, fs.getntmsuioptions, ntmsapi/GetNtmsUIOptions, ntmsapi/GetNtmsUIOptionsA, ntmsapi/GetNtmsUIOptionsW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNtmsUIOptionsW (Unicode) and GetNtmsUIOptionsA (ANSI)
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
 - GetNtmsUIOptionsW
 - ntmsapi/GetNtmsUIOptionsW
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
 - GetNtmsUIOptions
 - GetNtmsUIOptionsA
 - GetNtmsUIOptionsW
---

# GetNtmsUIOptionsW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>GetNtmsUIOptions</b> function obtains the list of computer names to which the specified type of user interface is being directed for the given object. A call to 
<b>GetNtmsUIOptions</b> returns the list of destinations for the instance determined by the <i>lpObjectId</i> and <i>dwType</i> parameters.

If there are no destinations in the list for the specified instance, the function returns ERROR_SUCCESS along with a list length of zero.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpObjectId [in]

Unique identifier of the object whose UI is being redirected. The object must be a container that can be a source for events. The object can be either be an application (a mount request triggered by the application), a library (a door open request in response to an eject) or a computer (all UI pertaining to the computer). 




To specify the computer container set the <i>lpObjectId</i> pointer to point to a buffer with the Removable Storage Manager's computer object GUID. To specify a particular library set it to point to a buffer with the library's GUID. To specify an application, pass in a <b>NULL</b> pointer. The identity of the application is determined by the session used in <i>hSession</i>. Note that an application can have multiple sessions open simultaneously. In this case, the value set applies only to the <i>hSession</i> session.

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

### -param lpszDestination [out]

Multi-string that returns the names of the machines to which the UI is being redirected. This parameter cannot be <b>NULL</b>.

### -param lpdwBufSize [in, out]

Size of the destination string, in <b>TCHARs</b>.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer size specified by <i>lpdwSize</i> is too small for the destinations found. The function returns the actual size in <i>lpdwSize</i>.

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
The <i>lpdwSize</i> or <i>lpszDestination</i> parameter is <b>NULL</b>, or <i>lpObjectId</i> is not a valid container, or <i>dwType</i> is not one of the three valid values.

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
<b>GetNtmsUIOptions</b> returns a list of destinations for a particular instance determined by the <i>lpObjectId</i> and <i>dwType</i> parameters.

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
 





> [!NOTE]
> The ntmsapi.h header defines GetNtmsUIOptions as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Library Control Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsuioptionsa">SetNtmsUIOptions</a>
