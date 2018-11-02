---
UID: NF:mprapi.MprConfigFilterGetInfo
title: MprConfigFilterGetInfo function
author: windows-sdk-content
description: Returns static filtering information for a specified transport protocol type.
old-location: rras\mprconfigfiltergetinfo.htm
tech.root: rras
ms.assetid: d3c35418-57f4-4000-93c2-c04b5b0140ff
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprConfigFilterGetInfo, MprConfigFilterGetInfo function [RAS], mprapi/MprConfigFilterGetInfo, rras.mprconfigfiltergetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigFilterGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprConfigFilterGetInfo function


## -description


The <b>MprConfigFilterGetInfo</b> function returns static filtering information for a specified  transport protocol type.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param dwLevel [in]

A <b>DWORD</b> value that describes the format in which the information is returned in the <i>lpBuffer</i> parameter. Must be zero.


### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport protocol type of the static filtering information in the <i>lpBuffer</i> parameter. Acceptable values for <i>dwTransportId</i> are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Transport (Protocol Family)</th>
</tr>
<tr>
<td>PID_ATALK</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>PID_IP</td>
<td>Internet Protocol version 4</td>
</tr>
<tr>
<td>PID_IPX</td>
<td>Internet Packet Exchange</td>
</tr>
<tr>
<td>PID_NBF</td>
<td>NetBIOS Frames Protocol</td>
</tr>
<tr>
<td>PID_IPV6</td>
<td>Windows Server 2008 or later: Internet Protocol version 6</td>
</tr>
</table>
 


### -param lpBuffer [out]

On successful completion, a pointer to a <a href="https://msdn.microsoft.com/f930b145-554b-40ea-ace0-60978ed428c1">MPR_FILTER_0</a> structure that contains the filter driver configuration information. Free this memory buffer by calling 
<a href="https://msdn.microsoft.com/d7df56ee-72e4-4b0c-87a3-a1f66d791b62">MprConfigBufferFree</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

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
<i>hMprConfig</i> or <i>lpBuffer</i> is <b>NULL</b>, or <i>dwLevel</i> is not set to 0.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f930b145-554b-40ea-ace0-60978ed428c1">MPR_FILTER_0</a>



<a href="https://msdn.microsoft.com/278cf536-3aed-4384-a9d8-ab8786a5cb1e">MprConfigFilterSetInfo</a>
 

 

