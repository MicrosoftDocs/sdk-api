---
UID: NF:scclient.CSecureChannelClient.GetAppSec
title: CSecureChannelClient::GetAppSec
author: windows-sdk-content
description: The GetAppSec method retrieves the application security levels of the local and remote components.
old-location: wmdm\csecurechannelclient_getappsec.htm
old-project: WMDM
ms.assetid: 69de42ad-293f-4c5a-8c5d-ada686fa68b2
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],GetAppSec method, CSecureChannelClient.GetAppSec, CSecureChannelClient::GetAppSec, CSecureChannelClientGetAppSec, GetAppSec, GetAppSec method [windows Media Device Manager], GetAppSec method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::GetAppSec, wmdm.csecurechannelclient_getappsec
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelClient.GetAppSec
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelClient::GetAppSec


## -description



The <b>GetAppSec</b> method retrieves the application security levels of the local and remote components.




## -parameters




### -param pdwLocalAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the local component (the application).


### -param pdwRemoteAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the remote component (typically the service provider).


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>
 

 

