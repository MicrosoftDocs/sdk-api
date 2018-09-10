---
UID: NF:winnetwk.WNetGetProviderNameA
title: WNetGetProviderNameA function
author: windows-sdk-content
description: The WNetGetProviderName function obtains the provider name for a specific type of network.
old-location: wnet\wnetgetprovidername.htm
tech.root: WNet
ms.assetid: c1369098-c574-4d5f-8051-ca5aa548e63f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WNetGetProviderName, WNetGetProviderName function [Windows Networking (WNet)], WNetGetProviderNameA, WNetGetProviderNameW, _win32_wnetgetprovidername, winnetwk/WNetGetProviderName, winnetwk/WNetGetProviderNameA, winnetwk/WNetGetProviderNameW, wnet.wnetgetprovidername
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetProviderNameW (Unicode) and WNetGetProviderNameA (ANSI)
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
 - WNetGetProviderName
 - WNetGetProviderNameA
 - WNetGetProviderNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WNetGetProviderNameA function


## -description


The
				<b>WNetGetProviderName</b> function obtains the provider name for a specific type of network.


## -parameters




### -param dwNetType [in]

Network type that is unique to the network. If two networks claim the same type, the function returns the name of the provider loaded first. Only the high word of the network type is used. If a network reports a subtype in the low word, it is ignored. 




You can find a complete list of network types in the header file Winnetwk.h.


### -param lpProviderName [out]

Pointer to a buffer that receives the network provider name.


### -param lpBufferSize [in, out]

Size of the buffer passed to the function, in characters. If the return value is ERROR_MORE_DATA, <i>lpBufferSize</i> returns the buffer size required (in characters) to hold the provider name. 




<b>Windows Me/98/95:  </b>The size of the buffer is in bytes, not characters. Also, the buffer must be at least 1 byte long.


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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to hold the network provider name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_NETWORK</b></dt>
</dl>
</td>
<td width="60%">
The network is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProviderName</i> parameter or the <i>lpBufferSize</i> parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/df190133-b73b-4f3e-aaee-4095cd619065">WNetGetNetworkInformation</a>



<a href="https://msdn.microsoft.com/19273874-adf1-4ffb-8b83-0eaa64e4622e">WNetGetResourceInformation</a>



<a href="https://msdn.microsoft.com/12c02092-f2d5-4477-92a7-ae075b8a243a">WNetGetUniversalName</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

