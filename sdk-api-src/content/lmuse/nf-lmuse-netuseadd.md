---
UID: NF:lmuse.NetUseAdd
title: NetUseAdd function
author: windows-driver-content
description: The NetUseAdd function establishes a connection between the local computer and a remote server.
old-location: netmgmt\netuseadd.htm
old-project: NetMgmt
ms.assetid: 22550c17-003a-4f59-80f0-58fa3e286844
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 1, 2, NetUseAdd, NetUseAdd function [Network Management], _win32_netuseadd, lmuse/NetUseAdd, netmgmt.netuseadd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmuse.h
req.include-header: Lm.h
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
-	NetUseAdd
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetUseAdd function


## -description


The
				<b>NetUseAdd</b> function establishes a connection between the local computer and a remote server. You can specify a local drive letter or a printer device to connect. If you do not specify a local drive letter or printer device, the function authenticates the client with the server for future connections.


## -parameters




### -param servername

TBD


### -param LevelFlags

TBD


### -param buf

TBD


### -param parm_err

TBD




#### - Buf [in]

A pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>Level</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


#### - Level [in]

A value that specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource. Information includes the connection status and type. The <i>Buf</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the connection between a local device and a shared resource. Information includes the connection status and type, and a user name and domain name. The <i>Buf</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a> structure.

</td>
</tr>
</table>
 


#### - ParmError [out]

A pointer to a value that receives the index of the first member of the information structure in error when the ERROR_INVALID_PARAMETER error is returned. If this parameter is <b>NULL</b>, the index is not returned on error. For more information, see the following Remarks section.


#### - UncServerName [in]

The UNC name of the computer on which to execute this function. If this parameter is <b>NULL</b>, then the local computer is used. If the <i>UncServerName</i> parameter specified is a remote computer, then the remote computer must support remote RPC calls using the legacy Remote Access Protocol mechanism. 

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



You can also use the 
<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a> and <a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a> functions to redirect a local device to a network resource.

No special group membership is required to call the 
<b>NetUseAdd</b> function. This function cannot be executed on a remote server except in cases of downlevel compatibility.

This function applies only to the Server Message Block (LAN Manager Workstation) client. The <b>NetUseAdd</b> function does not support Distributed File System (DFS) shares. To add a share using a different network provider (WebDAV or a DFS share, for example), use the <a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a> or <a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a> function.


If the 
<b>NetUseAdd</b> function returns ERROR_INVALID_PARAMETER, you can use the <i>ParmError</i> parameter to indicate the first member of the information structure that is invalid. (The information structure begins with USE_INFO_ and its format is specified by the <i>Level</i> parameter.) The following table lists the values that can be returned in the <i>ParmError</i> parameter and the corresponding structure member that is in error. (The prefix ui<i>*</i>_ indicates that the member can begin with multiple prefixes, for example, ui1_ or ui2_.)

<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Member</th>
</tr>
<tr>
<td>USE_LOCAL_PARMNUM</td>
<td>1</td>
<td>ui<i>*</i>_local</td>
</tr>
<tr>
<td>USE_REMOTE_PARMNUM</td>
<td>2</td>
<td>ui<i>*</i>_remote</td>
</tr>
<tr>
<td>USE_PASSWORD_PARMNUM</td>
<td>3</td>
<td>ui<i>*</i>_password</td>
</tr>
<tr>
<td>USE_ASGTYPE_PARMNUM</td>
<td>4</td>
<td>ui<i>*</i>_asg_type</td>
</tr>
<tr>
<td>USE_USERNAME_PARMNUM</td>
<td>5</td>
<td>ui<i>*</i>_username</td>
</tr>
<tr>
<td>USE_DOMAINNAME_PARMNUM</td>
<td>6</td>
<td>ui<i>*</i>_domainname</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/200b0640-71e9-4f60-bf4c-c8df10bfe095">NetUseDel</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/b9f680b8-b56a-42be-9af1-d7b18328ded4">USE_INFO_1</a>



<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>



<a href="https://msdn.microsoft.com/faec728c-f19e-418c-9bdb-cde93e7d98fb">WNetAddConnection2</a>



<a href="https://msdn.microsoft.com/169c7bb4-cb08-424c-af79-2133684a99db">WNetAddConnection3</a>
 

 

