---
UID: NF:lmuse.NetUseEnum
title: NetUseEnum function
author: windows-driver-content
description: The NetUseEnum function lists all current connections between the local computer and resources on remote servers.
old-location: netmgmt\netuseenum.htm
old-project: NetMgmt
ms.assetid: fb527f85-baea-48e8-b837-967870834ec5
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: NetUseEnum, NetUseEnum function [Network Management], _win32_netuseenum, lmuse/NetUseEnum, netmgmt.netuseenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmuse.h
req.include-header: Lm.h, Lmcons.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STAT_WORKSTATION_0, *PSTAT_WORKSTATION_0, *LPSTAT_WORKSTATION_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetUseEnum
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUseEnum function


## -description


The
				<b>NetUseEnum</b> function lists all current connections between the local computer and resources on remote servers.

You can also use the 
<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a> and the 
<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a> functions to enumerate network resources or connections.


## -parameters




### -param UncServerName [in]

The UNC name of the computer on which to execute this function. If this is parameter is <b>NULL</b>, then the local computer is used. If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism.  

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


### -param LevelFlags

TBD


### -param BufPtr [out]

A pointer to the buffer that receives the information structures. The format of this data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function when the information is no longer needed. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b>.


### -param PreferedMaximumSize [in]

The preferred maximum length, in bytes, of the data to return. If <b>MAX_PREFERRED_LENGTH</b> is specified, the function allocates the amount of memory required for the data. If another value is specified in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b>. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param EntriesRead [out]

A pointer to a value that receives the count of elements actually enumerated.


### -param TotalEntries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


### -param ResumeHandle [in, out]

A pointer to a value that contains a resume handle which is used to continue the search. The handle should be zero on the first call and left unchanged for subsequent calls. If <i>ResumeHandle</i> is <b>NULL</b>, then no resume handle is stored.


#### - Level [in]

The information level of the data requested. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Specifies a local device name and the share name of a remote resource. The <i>BufPtr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/86db3f19-84c5-4e89-82cb-f01d17dcf4ec">USE_INFO_0</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource, including connection status and type. The <i>BufPtr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a> structures.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource. Information includes the connection status, connection type, user name, and domain name. The <i>BufPtr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a> structures.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>BufPtr</i> or <i>entriesread</i> parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There is more data to return. This error is returned if the buffer size is insufficient to hold all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if the  <i>UncServerName</i> parameter was not <b>NULL</b> and the remote server does not support remote RPC calls using the legacy Remote Access Protocol mechanism. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



No special group membership is required to call the 
<b>NetUseEnum</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility using the legacy Remote Access Protocol.

To retrieve information about one network connection, you can call the 
<a href="https://msdn.microsoft.com/257875db-5ed9-4569-8dbb-5dcc7a6af95c">NetUseGetInfo</a> function.

This function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseEnum</b> function does not support Distributed File System (DFS) shares. To enumerate shares using a different network provider (WebDAV or a DFS share, for example), use the <a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>, <a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a>, and <a href="https://msdn.microsoft.com/c68fd9de-9f24-41f0-8b59-2d083fec8abf">WNetCloseEnum</a> functions.






## -see-also




<a href="https://msdn.microsoft.com/257875db-5ed9-4569-8dbb-5dcc7a6af95c">NetUseGetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/86db3f19-84c5-4e89-82cb-f01d17dcf4ec">USE_INFO_0</a>



<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a>



<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>



<a href="https://msdn.microsoft.com/c68fd9de-9f24-41f0-8b59-2d083fec8abf">WNetCloseEnum</a>



<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a>



<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>
 

 

