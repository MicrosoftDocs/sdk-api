---
UID: NF:winnetwk.WNetGetNetworkInformationW
title: WNetGetNetworkInformationW function
author: windows-sdk-content
description: The WNetGetNetworkInformation function returns extended information about a specific network provider whose name was returned by a previous network enumeration.
old-location: wnet\wnetgetnetworkinformation.htm
tech.root: WNet
ms.assetid: df190133-b73b-4f3e-aaee-4095cd619065
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WNetGetNetworkInformation, WNetGetNetworkInformation function [Windows Networking (WNet)], WNetGetNetworkInformationA, WNetGetNetworkInformationW, _win32_wnetgetnetworkinformation, winnetwk/WNetGetNetworkInformation, winnetwk/WNetGetNetworkInformationA, winnetwk/WNetGetNetworkInformationW, wnet.wnetgetnetworkinformation
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
- apiref
: 
- 
: 
- WNetGetNetworkInformationW
: 
---

# WNetGetNetworkInformationW function


## -description


The
				<b>WNetGetNetworkInformation</b> function returns extended information about a specific network provider whose name was returned by a previous network enumeration.


## -parameters




### -param lpProvider [in]

Pointer to a constant null-terminated string that contains the name of the network provider for which information is required.


### -param lpNetInfoStruct [out]

Pointer to a 
<a href="https://msdn.microsoft.com/2f60209f-7777-4130-b212-245673dd0055">NETINFOSTRUCT</a> structure. The structure describes characteristics of the network.


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




<a href="https://msdn.microsoft.com/2f60209f-7777-4130-b212-245673dd0055">NETINFOSTRUCT</a>



<a href="https://msdn.microsoft.com/c53d078e-188a-4371-bdb9-fc023bc0c1ba">NETRESOURCE</a>



<a href="https://msdn.microsoft.com/2c58c6d0-d5fe-447e-be39-df34072c160e">WNetEnumResource</a>



<a href="https://msdn.microsoft.com/c1369098-c574-4d5f-8051-ca5aa548e63f">WNetGetProviderName</a>



<a href="https://msdn.microsoft.com/d99a549a-bf27-497f-a3be-bbe2c668bf90">WNetOpenEnum</a>



<a href="https://msdn.microsoft.com/7668ac55-7104-4ddb-88eb-920cfe4e36fd">Windows
		  Networking (WNet) Overview</a>



<a href="https://msdn.microsoft.com/95e30f8f-a326-424d-bd80-5fc9b3078dad">Windows
		  Networking Functions</a>
 

 

