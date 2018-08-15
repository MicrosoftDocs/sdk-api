---
UID: NF:ntmsapi.CreateNtmsMediaPoolW
title: CreateNtmsMediaPoolW function
author: windows-sdk-content
description: The CreateNtmsMediaPool function creates a new application media pool.
old-location: fs\createntmsmediapool.htm
old-project: Rsm
ms.assetid: a55a8952-2b64-4082-9422-31484c7e777f
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CreateNtmsMediaPool, CreateNtmsMediaPool function [Files], CreateNtmsMediaPoolA, CreateNtmsMediaPoolW, NTMS_CREATE_NEW, NTMS_OPEN_ALWAYS, NTMS_OPEN_EXISTING, _zaw_createntmsmediapool, base.createntmsmediapool, fs.createntmsmediapool, ntmsapi/CreateNtmsMediaPool, ntmsapi/CreateNtmsMediaPoolA, ntmsapi/CreateNtmsMediaPoolW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntmsapi.h
req.include-header: 
req.redist: 
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
 - CreateNtmsMediaPool
 - CreateNtmsMediaPoolA
 - CreateNtmsMediaPoolW
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: ADAM
---

# CreateNtmsMediaPoolW function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CreateNtmsMediaPool</b> function creates a new application media pool.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpPoolName [in]

Name of the new media pool. Media pool names must be unique within the scope of a single RSM database.


### -param lpMediaType [in]

Identifier for the type of media in this media pool. Use the 
<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a> function to get a list of available media types and their attributes. The application can pass a <b>NULL</b> pointer to create a media pool that contains only other media pools.


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




## -see-also




<a href="https://msdn.microsoft.com/a0afe0ca-61ad-4ac8-8e3e-4a7e9ddd6600">AllocateNtmsMedia</a>



<a href="https://msdn.microsoft.com/79885083-beb6-4c66-8271-23082994a258">DeleteNtmsMediaPool</a>



<a href="https://msdn.microsoft.com/1d2168a3-077e-48fc-8a06-91952213f2cb">GetNtmsObjectSecurity</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540727(v=VS.85).aspx">Media Services Functions</a>



<a href="https://msdn.microsoft.com/ea6be316-6188-46a2-b12a-fe8426bc5fac">SetNtmsObjectSecurity</a>
 

 

