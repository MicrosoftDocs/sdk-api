---
UID: NF:adhoc.IDot11AdHocNetwork.GetSecuritySetting
title: IDot11AdHocNetwork::GetSecuritySetting
author: windows-sdk-content
description: Gets the security settings for the network.
old-location: nwifi\idot11adhocnetwork_getsecuritysetting.htm
old-project: nativewifi
ms.assetid: 3e5fa757-41fd-4541-a16e-15c2fb66e15a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetSecuritySetting, GetSecuritySetting method [NativeWIFI], GetSecuritySetting method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetSecuritySetting method, IDot11AdHocNetwork.GetSecuritySetting, IDot11AdHocNetwork::GetSecuritySetting, adhoc/IDot11AdHocNetwork::GetSecuritySetting, nwifi.idot11adhocnetwork_getsecuritysetting
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork.GetSecuritySetting
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork::GetSecuritySetting


## -description


Gets the security settings for the network.


## -parameters




### -param pAdHocSecuritySetting [out]

A pointer to an <a href="https://msdn.microsoft.com/55b78a98-ad25-4646-b325-73d770d602b3">IDot11AdHocSecuritySettings</a> interface that contains the security settings for the network.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a>
 

 

