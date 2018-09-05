---
UID: NF:lmwksta.NetWkstaTransportEnum
title: NetWkstaTransportEnum function
author: windows-sdk-content
description: The NetWkstaTransportEnum function supplies information about transport protocols that are managed by the redirector, which is the software on the client computer that generates file requests to the server computer.
old-location: netmgmt\netwkstatransportenum.htm
old-project: netmgmt
ms.assetid: 08bd22a9-00a7-4563-9353-c070ca9b2500
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, NetWkstaTransportEnum, NetWkstaTransportEnum function [Network Management], _win32_netwkstatransportenum, lmwksta/NetWkstaTransportEnum, netmgmt.netwkstatransportenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmwksta.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: USE_INFO_3, *PUSE_INFO_3, *LPUSE_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetWkstaTransportEnum
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetWkstaTransportEnum function


## -description


The 
				<b>NetWkstaTransportEnum</b> function supplies information about transport protocols that are managed by the redirector, which is the software on the client computer that generates file requests to the server computer.


## -parameters




### -param servername [in]

A pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.
					


### -param level [in]

The level of information requested for the data. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Return workstation transport protocol information. The <i>bufptr</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/e7afe2a3-f729-4fd5-afc3-d3ffbd09e884">WKSTA_TRANSPORT_INFO_0</a> structures.

</td>
</tr>
</table>
 


### -param bufptr [out]

A pointer to the buffer that receives the data. The format of this data depends on the value of the <i>level</i> parameter. This buffer is allocated by the system and must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with <b>ERROR_MORE_DATA</b> or <b>NERR_BufTooSmall</b>.


### -param prefmaxlen [in]

The preferred maximum length of returned data, in bytes. If you specify <b>MAX_PREFERRED_LENGTH</b>, the function allocates the amount of memory required for the data. If you specify another value in this parameter, it can restrict the number of bytes that the function returns. If the buffer size is insufficient to hold all entries, the function returns <b>ERROR_MORE_DATA</b> or <b>NERR_BufTooSmall</b>. For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


### -param entriesread [out]

A pointer to a value that receives the count of elements actually enumerated.


### -param totalentries [out]

A pointer to a value that receives the total number of entries that could have been enumerated from the current resume position. Note that applications should consider this value only as a hint.


#### - resume_handle [in, out]

A pointer to a value that contains a resume handle which is used to continue an existing workstation transport search. The handle should be zero on the first call and left unchanged for subsequent calls. If the <i>resumehandle</i> parameter is a <b>NULL</b> pointer, no resume handle is stored.


#### - resumehandle [in, out]

A pointer to a value that contains a resume handle which is used to continue an existing workstation transport search. The handle should be zero on the first call and left unchanged for subsequent calls. If the <i>resumehandle</i> parameter is a <b>NULL</b> pointer, no resume handle is stored.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The level parameter, which indicates what level of data structure information is available, is invalid. This error is returned if the <i>level</i> parameter is specified as a value other than zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid. This error is returned if the <i>bufptr</i> or the <i>entriesread</i> parameters are <b>NULL</b> pointers. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory was available to process the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if a remote server was specified in <i>servername</i> parameter, and this request is not supported on the remote server. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_BufTooSmall</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. Specify a large enough buffer to receive all entries. This error code is defined in the <i>Lmerr.h</i> header file.

</td>
</tr>
</table>
 




## -remarks



No special group membership is required to successfully execute the 
<b>NetWkstaTransportEnum</b> function.




## -see-also




<a href="https://msdn.microsoft.com/016060ea-eae1-421f-b708-5c2ddd2000c1">NetWkstaTransportAdd</a>



<a href="https://msdn.microsoft.com/6d0ec459-8d7b-41fe-96dd-203e6a42164f">NetWkstaTransportDel</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>



<a href="https://msdn.microsoft.com/e7afe2a3-f729-4fd5-afc3-d3ffbd09e884">WKSTA_TRANSPORT_INFO_0</a>
 

 

