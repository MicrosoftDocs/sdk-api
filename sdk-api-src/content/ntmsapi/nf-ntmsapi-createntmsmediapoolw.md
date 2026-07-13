---
UID: NF:ntmsapi.CreateNtmsMediaPoolW
title: CreateNtmsMediaPoolW function (ntmsapi.h)
description: The CreateNtmsMediaPoolW (Unicode) function creates a new application media pool. (CreateNtmsMediaPoolW)
helpviewer_keywords: ["CreateNtmsMediaPool", "CreateNtmsMediaPool function [Files]", "CreateNtmsMediaPoolW", "NTMS_CREATE_NEW", "NTMS_OPEN_ALWAYS", "NTMS_OPEN_EXISTING", "_zaw_createntmsmediapool", "base.createntmsmediapool", "fs.createntmsmediapool", "ntmsapi/CreateNtmsMediaPool", "ntmsapi/CreateNtmsMediaPoolW"]
old-location: fs\createntmsmediapool.htm
tech.root: fs
ms.assetid: a55a8952-2b64-4082-9422-31484c7e777f
ms.date: 08/03/2022
ms.keywords: CreateNtmsMediaPool, CreateNtmsMediaPool function [Files], CreateNtmsMediaPoolA, CreateNtmsMediaPoolW, NTMS_CREATE_NEW, NTMS_OPEN_ALWAYS, NTMS_OPEN_EXISTING, _zaw_createntmsmediapool, base.createntmsmediapool, fs.createntmsmediapool, ntmsapi/CreateNtmsMediaPool, ntmsapi/CreateNtmsMediaPoolA, ntmsapi/CreateNtmsMediaPoolW
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateNtmsMediaPoolW (Unicode) and CreateNtmsMediaPoolA (ANSI)
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
 - CreateNtmsMediaPoolW
 - ntmsapi/CreateNtmsMediaPoolW
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
 - CreateNtmsMediaPool
 - CreateNtmsMediaPoolA
 - CreateNtmsMediaPoolW
---

# CreateNtmsMediaPoolW function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CreateNtmsMediaPool</b> function creates a new application media pool.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param lpPoolName [in]

Name of the new media pool. Media pool names must be unique within the scope of a single RSM database.

### -param lpMediaType [in]

Identifier for the type of media in this media pool. Use the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-enumeratentmsobject">EnumerateNtmsObject</a> function to get a list of available media types and their attributes. The application can pass a <b>NULL</b> pointer to create a media pool that contains only other media pools.

### -param dwAction [in]

Action to perform. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPEN_EXISTING"></a><a id="ntms_open_existing"></a><dl>
<dt><b>NTMS_OPEN_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing media pool by name. Returns ERROR_OBJECT_NOT_FOUND if the pool does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_OPEN_ALWAYS"></a><a id="ntms_open_always"></a><dl>
<dt><b>NTMS_OPEN_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Opens an existing media pool or creates the pool if it does not exist.

</td>
</tr>
<tr>
<td width="40%"><a id="NTMS_CREATE_NEW"></a><a id="ntms_create_new"></a><dl>
<dt><b>NTMS_CREATE_NEW</b></dt>
</dl>
</td>
<td width="60%">
Creates a new media pool. Returns ERROR_ALREADY_EXISTS if the pool exists.

</td>
</tr>
</table>

### -param lpSecurityAttributes [in]

Optional security descriptor used to restrict access to the pool.

### -param lpPoolId [out]

Pointer to a variable that receives the unique identifier of the media pool after the media pool is successfully created or opened.

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
NTMS_CONTROL_ACCESS to the root pool or the parent media pool is denied while trying to create a new media pool. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>NTMS_MODIFY_ACCESS to the parent media pool is denied while trying to create a new media pool. Other security errors are also possible, but they would indicate a security subsystem error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Unable to create a new media pool because one already exists with this name.

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
The database is full. Other security errors are also possible, but they would indicate a security subsystem error.

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
<dt><b>ERROR_INVALID_MEDIA</b></dt>
</dl>
</td>
<td width="60%">
The selected media type is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The pool name syntax is not valid. (The name is too long.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The media pool name or media pool ID pointer is missing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Unable to open existing media pool.

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

Free, Unrecognized, and Import media pools are created by RSM and cannot be created with the 
<b>CreateNtmsMediaPool</b> function.

RSM media pools are organized as a hierarchy separated by the "\" character. Application, Free, Unrecognized, and Import media pools exist at the root of the hierarchy. RSM creates and manages the Free, Unrecognized, and Import pools. RSM creates a Free media pool for each media type available.

Application-specific media pools are created by applications. Applications create media pools for their own use under the root application pool. These media pools have file system-like names. Only the end-point of the name contains media and policy. An application can define pools such as \MyApp\Pool1 and \MyApp\Pool2. This conveys the hierarchy to the user interface and avoids duplicate names. Each pool level must be created individually; first MyApp and then Pool1 and Pool2, much like folders and files.

<b>Windows Server 2003:  </b>To create a media pool, you must have NTMS_CONTROL_ACCESS to the root pool and parent pool. If a security descriptor is not provided, the pool inherits the ACEs of its parent pool (if the parent pool is not the root pool). In addition, the creator and local system accounts have full access to the pool. If the parent pool is the root pool, its ACEs are not inherited; the only ACEs in the DACL are full access for the creator and local system accounts.





> [!NOTE]
> The ntmsapi.h header defines CreateNtmsMediaPool as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/rsm/media">AllocateNtmsMedia</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-deletentmsmediapool">DeleteNtmsMediaPool</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-getntmsobjectsecurity">GetNtmsObjectSecurity</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Media Services Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-setntmsobjectsecurity">SetNtmsObjectSecurity</a>
