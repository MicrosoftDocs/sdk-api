---
UID: NF:winnetwk.WNetEnumResourceA
title: WNetEnumResourceA function (winnetwk.h)
author: windows-sdk-content
description: The WNetEnumResource function continues an enumeration of network resources that was started by a call to the WNetOpenEnum function.
old-location: wnet\wnetenumresource.htm
tech.root: WNet
ms.assetid: 2c58c6d0-d5fe-447e-be39-df34072c160e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WNetEnumResource, WNetEnumResource function [Windows Networking (WNet)], WNetEnumResourceA, WNetEnumResourceW, _win32_wnetenumresource, winnetwk/WNetEnumResource, winnetwk/WNetEnumResourceA, winnetwk/WNetEnumResourceW, wnet.wnetenumresource
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetEnumResourceW (Unicode) and WNetEnumResourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mpr.lib
req.dll: Mpr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mpr.dll
api_name:
 - WNetEnumResource
 - WNetEnumResourceA
 - WNetEnumResourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetEnumResourceA function


## -description


The
				<b>WNetEnumResource</b> function continues an enumeration of network resources that was started by a call to the 
<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a> function.


## -parameters




### -param hEnum [in]

Handle that identifies an enumeration instance. This handle must be returned by the 
<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a> function.


### -param lpcCount [in, out]

Pointer to a variable specifying the number of entries requested. If the number requested is –1, the function returns as many entries as possible. 




If the function succeeds, on return the variable pointed to by this parameter contains the number of entries actually read.


### -param lpBuffer [out]

Pointer to the buffer that receives the enumeration results. The results are returned as an array of 
<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a> structures. Note that the buffer you allocate must be large enough to hold the structures, plus the strings to which their members point. For more information, see the following Remarks section. 




The buffer is valid until the next call using the handle specified by the <i>hEnum</i> parameter. The order of 
<b>NETRESOURCE</b> structures in the array is not predictable.


### -param lpBufferSize [in, out]

Pointer to a variable that specifies the size of the <i>lpBuffer</i> parameter, in bytes. If the buffer is too small to receive even one entry, this parameter receives the required size of the buffer.


## -returns



If the function succeeds, the return value is one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The enumeration succeeded, and the buffer contains the requested data. The calling application can continue to call 
<b>WNetEnumResource</b> to complete the enumeration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more entries. The buffer contents are undefined.

</td>
</tr>
</table>
 

If the function fails, the return value is a 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>, such as one of the following values.

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
More entries are available with subsequent calls. For more information, see the following Remarks section.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hEnum</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable. (This condition is tested before <i>hEnum</i> is tested for validity.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
A network-specific error occurred. To obtain a description of the error, call the 
<a href="https://msdn.microsoft.com/8e13c467-adcf-4e97-b51a-1f5fc919b51e">WNetGetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WNetEnumResource</b> function does not enumerate users connected to a share; you can call the 
<a href="https://msdn.microsoft.com/935ac6e9-78e0-42ae-a454-0a14b03ddc21">NetConnectionEnum</a> function to accomplish this task. To enumerate hidden shares, call the 
<a href="https://msdn.microsoft.com/9114c54d-3905-4d40-9162-b3ea605f6fcb">NetShareEnum</a> function.

An application cannot set the <i>lpBuffer</i> parameter to <b>NULL</b> and retrieve the required buffer size from the <i>lpBufferSize</i> parameter. Instead, the application should allocate a buffer of a reasonable size—16 kilobytes is typical—and use the value of <i>lpBufferSize</i> for error detection.


#### Examples

For a code sample that illustrates an application-defined function that enumerates all the resources on a network, see 
<a href="https://msdn.microsoft.com/f5872ee7-483d-406a-b7d8-4ce93613fd29">Enumerating Network Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>



<a href="https://msdn.microsoft.com/c68fd9de-9f24-41f0-8b59-2d083fec8abf">WNetCloseEnum</a>



<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

