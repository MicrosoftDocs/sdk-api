---
UID: NF:wsddisco.IWSDiscoveryProvider.Detach
title: IWSDiscoveryProvider::Detach
author: windows-sdk-content
description: Detaches a callback interface from the discovery provider.
old-location: ncd\iwsdiscoveryprovider_detach_method.htm
old-project: wsdapi
ms.assetid: 562e7618-06ac-4bd3-9746-6ff3a7531b6b
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: Detach, Detach method, Detach method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,Detach method, IWSDiscoveryProvider.Detach, IWSDiscoveryProvider::Detach, ncd.iwsdiscoveryprovider_detach_method, wsddisco/IWSDiscoveryProvider::Detach
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
 - IWSDiscoveryProvider.Detach
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider::Detach


## -description


Detaches a callback interface from the discovery provider.


## -parameters






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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has not been attached. You must call <a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a> before calling this method.

</td>
</tr>
</table>
 




## -remarks



If a callback interface has been attached to a discovery provider via the <a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a> method, then <b>Detach</b> must be called before releasing the reference to the provider interface object.

The <b>Detach</b> operation blocks until all callbacks into the associated <a href="https://msdn.microsoft.com/e186f721-14d9-4d9b-942a-1c05ada2bee6">IWSDiscoveryProviderNotify</a> object have completed.




## -see-also




<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

