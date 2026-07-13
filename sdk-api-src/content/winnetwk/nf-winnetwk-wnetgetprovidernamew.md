---
UID: NF:winnetwk.WNetGetProviderNameW
title: WNetGetProviderNameW function (winnetwk.h)
description: The WNetGetProviderName function obtains the provider name for a specific type of network. (Unicode)
helpviewer_keywords: ["WNetGetProviderName", "WNetGetProviderName function [Windows Networking (WNet)]", "WNetGetProviderNameW", "_win32_wnetgetprovidername", "winnetwk/WNetGetProviderName", "winnetwk/WNetGetProviderNameW", "wnet.wnetgetprovidername"]
old-location: wnet\wnetgetprovidername.htm
tech.root: WNet
ms.assetid: c1369098-c574-4d5f-8051-ca5aa548e63f
ms.date: 12/05/2018
ms.keywords: WNetGetProviderName, WNetGetProviderName function [Windows Networking (WNet)], WNetGetProviderNameA, WNetGetProviderNameW, _win32_wnetgetprovidername, winnetwk/WNetGetProviderName, winnetwk/WNetGetProviderNameA, winnetwk/WNetGetProviderNameW, wnet.wnetgetprovidername
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNetGetProviderNameW
 - winnetwk/WNetGetProviderNameW
dev_langs:
 - c++
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
---

# WNetGetProviderNameW function


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
<a href="/windows/desktop/Debug/system-error-codes">system error code</a>, such as one of the following values.

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

<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa">WNetGetNetworkInformation</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa">WNetGetResourceInformation</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea">WNetGetUniversalName</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines WNetGetProviderName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
