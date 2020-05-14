---
UID: NF:winnetwk.WNetEnumResourceA
title: WNetEnumResourceA function (winnetwk.h)
description: The WNetEnumResource function continues an enumeration of network resources that was started by a call to the WNetOpenEnum function.
helpviewer_keywords: ["WNetEnumResource","WNetEnumResource function [Windows Networking (WNet)]","WNetEnumResourceA","WNetEnumResourceW","_win32_wnetenumresource","winnetwk/WNetEnumResource","winnetwk/WNetEnumResourceA","winnetwk/WNetEnumResourceW","wnet.wnetenumresource"]
old-location: wnet\wnetenumresource.htm
tech.root: WNet
ms.assetid: 2c58c6d0-d5fe-447e-be39-df34072c160e
ms.date: 12/05/2018
ms.keywords: WNetEnumResource, WNetEnumResource function [Windows Networking (WNet)], WNetEnumResourceA, WNetEnumResourceW, _win32_wnetenumresource, winnetwk/WNetEnumResource, winnetwk/WNetEnumResourceA, winnetwk/WNetEnumResourceW, wnet.wnetenumresource
f1_keywords:
- winnetwk/WNetEnumResource
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WNetEnumResourceA function


## -description


The
				<b>WNetEnumResource</b> function continues an enumeration of network resources that was started by a call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a> function.


## -parameters




### -param hEnum [in]

Handle that identifies an enumeration instance. This handle must be returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a> function.


### -param lpcCount [in, out]

Pointer to a variable specifying the number of entries requested. If the number requested is –1, the function returns as many entries as possible. 




If the function succeeds, on return the variable pointed to by this parameter contains the number of entries actually read.


### -param lpBuffer [out]

Pointer to the buffer that receives the enumeration results. The results are returned as an array of 
<a href="/windows/win32/api/winnetwk/ns-winnetwk-netresourcea">NETRESOURCE</a> structures. Note that the buffer you allocate must be large enough to hold the structures, plus the strings to which their members point. For more information, see the following Remarks section. 




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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

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
<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetlasterrora">WNetGetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



The 
<b>WNetEnumResource</b> function does not enumerate users connected to a share; you can call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum">NetConnectionEnum</a> function to accomplish this task. To enumerate hidden shares, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/lmshare/nf-lmshare-netshareenum">NetShareEnum</a> function.

An application cannot set the <i>lpBuffer</i> parameter to <b>NULL</b> and retrieve the required buffer size from the <i>lpBufferSize</i> parameter. Instead, the application should allocate a buffer of a reasonable size—16 kilobytes is typical—and use the value of <i>lpBufferSize</i> for error detection.


#### Examples

For a code sample that illustrates an application-defined function that enumerates all the resources on a network, see 
<a href="https://docs.microsoft.com/windows/desktop/WNet/enumerating-network-resources">Enumerating Network Resources</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetcloseenum">WNetCloseEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
 

 

