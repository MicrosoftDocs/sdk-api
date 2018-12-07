---
UID: NF:adhoc.IDot11AdHocManager.GetNetwork
title: IDot11AdHocManager::GetNetwork
author: windows-sdk-content
description: Returns the network associated with a signature.
old-location: nwifi\idot11adhocmanager_getnetwork.htm
tech.root: NativeWiFi
ms.assetid: 971703dc-1a3c-4c9a-a9e2-c547c96beacd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNetwork, GetNetwork method [NativeWIFI], GetNetwork method [NativeWIFI],IDot11AdHocManager interface, IDot11AdHocManager interface [NativeWIFI],GetNetwork method, IDot11AdHocManager.GetNetwork, IDot11AdHocManager::GetNetwork, adhoc/IDot11AdHocManager::GetNetwork, nwifi.idot11adhocmanager_getnetwork
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocManager.GetNetwork
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocManager::GetNetwork


## -description


Returns the network associated with a signature. 


## -parameters




### -param NetworkSignature [in]

A signature that uniquely identifies an ad hoc network. This signature is generated  from certain network attributes.


### -param pNetwork [out]

A pointer to an <a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a> interface that represents the network associated with the signature. 


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dcb93b9c-3292-4cbf-9d44-5367bdbd4878">IDot11AdHocManager</a>
 

 

