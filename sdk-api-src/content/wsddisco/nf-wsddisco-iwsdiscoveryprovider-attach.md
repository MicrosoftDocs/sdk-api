---
UID: NF:wsddisco.IWSDiscoveryProvider.Attach
title: IWSDiscoveryProvider::Attach
author: windows-sdk-content
description: Attaches a callback interface to the discovery provider.
old-location: ncd\iwsdiscoveryprovider_attach_method.htm
old-project: wsdapi
ms.assetid: 3bb2aead-b082-4a2b-b4bf-97a1feb1e11e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Attach, Attach method, Attach method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,Attach method, IWSDiscoveryProvider.Attach, IWSDiscoveryProvider::Attach, ncd.iwsdiscoveryprovider_attach_method, wsddisco/IWSDiscoveryProvider::Attach
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProvider.Attach
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider::Attach


## -description


Attaches a callback interface to the discovery provider.


## -parameters




### -param pSink [in]

Interface to receive callback notifications.  Search results as well as the Hello and Bye messages are communicated to this interface via the callbacks.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pSink</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has already been attached to the provider.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  Attach must be called before any other <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>method is used, except for <a href="https://msdn.microsoft.com/33b13cd5-ea60-4928-a220-db563c00a43c">SetAddressFamily</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

