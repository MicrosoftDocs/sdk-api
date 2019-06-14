---
UID: NF:winnetwk.WNetGetNetworkInformationA
title: WNetGetNetworkInformationA function (winnetwk.h)
author: windows-sdk-content
description: The WNetGetNetworkInformation function returns extended information about a specific network provider whose name was returned by a previous network enumeration.
old-location: wnet\wnetgetnetworkinformation.htm
tech.root: WNet
ms.assetid: df190133-b73b-4f3e-aaee-4095cd619065
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WNetGetNetworkInformation, WNetGetNetworkInformation function [Windows Networking (WNet)], WNetGetNetworkInformationA, WNetGetNetworkInformationW, _win32_wnetgetnetworkinformation, winnetwk/WNetGetNetworkInformation, winnetwk/WNetGetNetworkInformationA, winnetwk/WNetGetNetworkInformationW, wnet.wnetgetnetworkinformation
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/ns-winnetwk-_netinfostruct">NETINFOSTRUCT</a> structure. The structure describes characteristics of the network.


## -returns



If the function succeeds, the return value is NO_ERROR.

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




<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/ns-winnetwk-_netinfostruct">NETINFOSTRUCT</a>



<a href="https://docs.microsoft.com/windows/desktop/api//rrascfg/nn-rrascfg-ieapproviderconfig">NETRESOURCE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetenumresourcea">WNetEnumResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetprovidernamea">WNetGetProviderName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnetwk/nf-winnetwk-wnetopenenuma">WNetOpenEnum</a>



<a href="https://docs.microsoft.com/windows/desktop/WNet/windows-networking-wnet-">Windows
		  Networking (WNet) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/WNet/windows-networking-functions">Windows
		  Networking Functions</a>
 

 

