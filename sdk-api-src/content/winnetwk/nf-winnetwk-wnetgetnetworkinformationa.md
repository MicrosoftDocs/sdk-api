---
UID: NF:winnetwk.WNetGetNetworkInformationA
title: WNetGetNetworkInformationA function (winnetwk.h)
description: The WNetGetNetworkInformation function returns extended information about a specific network provider whose name was returned by a previous network enumeration. (ANSI)
helpviewer_keywords: ["WNetGetNetworkInformationA", "winnetwk/WNetGetNetworkInformationA"]
old-location: wnet\wnetgetnetworkinformation.htm
tech.root: WNet
ms.assetid: df190133-b73b-4f3e-aaee-4095cd619065
ms.date: 12/05/2018
ms.keywords: WNetGetNetworkInformation, WNetGetNetworkInformation function [Windows Networking (WNet)], WNetGetNetworkInformationA, WNetGetNetworkInformationW, _win32_wnetgetnetworkinformation, winnetwk/WNetGetNetworkInformation, winnetwk/WNetGetNetworkInformationA, winnetwk/WNetGetNetworkInformationW, wnet.wnetgetnetworkinformation
req.header: winnetwk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WNetGetNetworkInformationW (Unicode) and WNetGetNetworkInformationA (ANSI)
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
 - WNetGetNetworkInformationA
 - winnetwk/WNetGetNetworkInformationA
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
 - WNetGetNetworkInformation
 - WNetGetNetworkInformationA
 - WNetGetNetworkInformationW
---

# WNetGetNetworkInformationA function


## -description

The
				<b>WNetGetNetworkInformation</b> function returns extended information about a specific network provider whose name was returned by a previous network enumeration.

## -parameters

### -param lpProvider [in]

Pointer to a constant null-terminated string that contains the name of the network provider for which information is required.

### -param lpNetInfoStruct [out]

Pointer to a 
<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netinfostruct">NETINFOSTRUCT</a> structure. The structure describes characteristics of the network.

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
<dt><b>ERROR_BAD_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpProvider</i> parameter does not match any running network provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The <b>cbStructure</b> member of the 
<b>NETINFOSTRUCT</b> structure does not contain a valid structure size.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnetwk/ns-winnetwk-netinfostruct">NETINFOSTRUCT</a>



<a href="ns-winnetwk-netresourcea.md">NETRESOURCE</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetprovidernamea">WNetGetProviderName</a>



<a href="/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a>



<a href="/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>

## -remarks

> [!NOTE]
> The winnetwk.h header defines WNetGetNetworkInformation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
