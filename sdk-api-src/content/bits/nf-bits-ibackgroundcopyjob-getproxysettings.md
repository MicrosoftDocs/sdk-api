---
UID: NF:bits.IBackgroundCopyJob.GetProxySettings
title: IBackgroundCopyJob::GetProxySettings
author: windows-sdk-content
description: Retrieves the proxy information that the job uses to transfer the files.
old-location: bits\ibackgroundcopyjob_getproxysettings.htm
old-project: bits
ms.assetid: c2d0ec9b-eaa1-4f78-9ccc-4e91d045cd94
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetProxySettings, GetProxySettings method [BITS], GetProxySettings method [BITS],IBackgroundCopyJob interface, IBackgroundCopyJob interface [BITS],GetProxySettings method, IBackgroundCopyJob.GetProxySettings, IBackgroundCopyJob::GetProxySettings, _drz_ibackgroundcopyjob_getproxysettings, bits.ibackgroundcopyjob_getproxysettings, bits/IBackgroundCopyJob::GetProxySettings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bits.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BG_JOB_PROXY_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - QmgrPrxy.dll
api_name:
 - IBackgroundCopyJob.GetProxySettings
product: Windows
targetos: Windows
req.lib: Bits.lib
req.dll: QmgrPrxy.dll
req.irql: 
---

# IBackgroundCopyJob::GetProxySettings


## -description


Retrieves the proxy information that the job uses to transfer the files.


## -parameters




### -param pProxyUsage [out]

Specifies the proxy settings the job uses to transfer the files. For a list of proxy options, see the 
<a href="https://msdn.microsoft.com/en-us/library/Aa362807(v=VS.85).aspx">BG_JOB_PROXY_USAGE</a> enumeration.


### -param pProxyList




### -param pProxyBypassList






#### - ppProxyBypassList [out]

Null-terminated string that contains an optional list of host names or IP addresses, or both, that were not routed through the proxy. The list is space-delimited. For details on the format of the string, see the Listing the Proxy Bypass section of 
<a href="https://msdn.microsoft.com/en-us/library/Aa383996(v=VS.85).aspx">Enabling Internet Functionality</a>. Call the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>ppProxyBypassList</i> when done.


#### - ppProxyList [out]

Null-terminated string that contains one or more proxies to use to transfer files. The list is space-delimited. For details on the format of the string, see the Listing Proxy Servers section of 
<a href="https://msdn.microsoft.com/en-us/library/Aa383996(v=VS.85).aspx">Enabling Internet Functionality</a>. Call the 
<a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free <i>ppProxyList</i> when done.


## -returns



This method returns the following <b>HRESULT</b> values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Proxy information was successfully retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362807(v=VS.85).aspx">BG_JOB_PROXY_USAGE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363047(v=VS.85).aspx">IBackgroundCopyJob::SetProxySettings</a>
 

 

