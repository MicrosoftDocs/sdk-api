---
UID: NF:wsddisco.IWSDiscoveryProvider.GetXMLContext
title: IWSDiscoveryProvider::GetXMLContext
author: windows-sdk-content
description: Gets the XML context associated with this provider.
old-location: ncd\iwsdiscoveryprovider_getxmlcontext.htm
old-project: WsdApi
ms.assetid: ee2a862a-9d1d-4099-982e-259b6ab815f6
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetXMLContext, GetXMLContext method, GetXMLContext method,IWSDiscoveryProvider interface, IWSDiscoveryProvider interface,GetXMLContext method, IWSDiscoveryProvider.GetXMLContext, IWSDiscoveryProvider::GetXMLContext, ncd.iwsdiscoveryprovider_getxmlcontext, wsddisco/IWSDiscoveryProvider::GetXMLContext
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDiscoveryProvider.GetXMLContext
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProvider::GetXMLContext


## -description


Gets the  XML context associated with this provider.


## -parameters




### -param ppContext [out]

Pointer to a pointer variable containing the XML context.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppContext</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The discovery provider has not been created. Call <a href="https://msdn.microsoft.com/44275cbe-ea02-41fd-b88d-81d4df966067">WSDCreateDiscoveryProvider</a> to create a provider.

</td>
</tr>
</table>
 




## -remarks



Returns an optional context for the XML state of the transaction. If the service layer is used then this should be the context the XML namespaces and types were registered with.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a> must be called before any other <a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
		 method is used.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a>



<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

