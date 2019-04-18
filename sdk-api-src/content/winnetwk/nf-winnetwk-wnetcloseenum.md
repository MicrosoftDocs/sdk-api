---
UID: NF:winnetwk.WNetCloseEnum
title: WNetCloseEnum function (winnetwk.h)
author: windows-sdk-content
description: The WNetCloseEnum function ends a network resource enumeration started by a call to the WNetOpenEnum function.
old-location: wnet\wnetcloseenum.htm
tech.root: WNet
ms.assetid: c68fd9de-9f24-41f0-8b59-2d083fec8abf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WNetCloseEnum, WNetCloseEnum function [Windows Networking (WNet)], _win32_wnetcloseenum, winnetwk/WNetCloseEnum, wnet.wnetcloseenum
ms.topic: function
req.header: winnetwk.h
req.include-header: 
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
 - WNetCloseEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WNetCloseEnum function


## -description


The
				<b>WNetCloseEnum</b> function ends a network resource enumeration started by a call to the 
<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a> function.


## -parameters




### -param hEnum [in]

Handle that identifies an enumeration instance. This handle must be returned by the 
<b>WNetOpenEnum</b> function.


## -returns



If the function succeeds, the return value is NO_ERROR.

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
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable. (This condition is tested before the handle specified in the <i>hEnum</i> parameter is tested for validity.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hEnum</i> parameter does not specifiy a valid handle.

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
 




## -see-also




<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a>



<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

