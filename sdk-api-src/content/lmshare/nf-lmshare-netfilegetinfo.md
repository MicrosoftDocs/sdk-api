---
UID: NF:lmshare.NetFileGetInfo
title: NetFileGetInfo function
author: windows-sdk-content
description: Retrieves information about a particular opening of a server resource.
old-location: fs\netfilegetinfo.htm
old-project: NetShare
ms.assetid: d50c05e7-7ddd-4a7d-96f6-51878e52373c
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: 2, 3, NetFileGetInfo, NetFileGetInfo function [Files], _win32_netfilegetinfo, fs.netfilegetinfo, lmshare/NetFileGetInfo, netmgmt.netfilegetinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
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
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetFileGetInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetFileGetInfo function


## -description


Retrieves information about a particular opening of a server resource.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param fileid [in]

Specifies the file identifier of the open resource for which to return information. The value of this parameter must have been returned in a previous enumeration call. For more information, see the following Remarks section.


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return the file identification number. The <i>bufptr</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/c80090d5-7064-4809-9185-02116f7ac2ef">FILE_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return the file identification number and other information about the file. The <i>bufptr</i> parameter is a pointer to a 
<a href="https://msdn.microsoft.com/67f5fa89-12c7-46fb-a118-de4bfed96923">FILE_INFO_3</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [out]

Pointer to the address of the buffer that receives the information. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
The supplied buffer is too small.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetFileGetInfo</b> function.

You can call the 
<a href="https://msdn.microsoft.com/1375b337-efb0-4be1-94f7-473456a825b5">NetFileEnum</a> function to retrieve information about multiple files open on a server.

If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling 
<b>NetFileGetInfo</b>. For more information, see 
<a href="https://msdn.microsoft.com/217749a4-55dc-457f-8582-1513ff3b0666">IADsResource</a> and 
<a href="https://msdn.microsoft.com/91335658-8efb-4945-9862-f72e78d749d6">IADsFileServiceOperations</a>.




## -see-also




<a href="https://msdn.microsoft.com/c80090d5-7064-4809-9185-02116f7ac2ef">FILE_INFO_2</a>



<a href="https://msdn.microsoft.com/67f5fa89-12c7-46fb-a118-de4bfed96923">FILE_INFO_3</a>



<a href="https://msdn.microsoft.com/cbcdad6e-80dd-49f0-9d69-a82a7010f10b">NetFile
		  Functions</a>



<a href="https://msdn.microsoft.com/1375b337-efb0-4be1-94f7-473456a825b5">NetFileEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

