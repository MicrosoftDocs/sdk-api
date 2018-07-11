---
UID: NF:wsddisco.IWSDiscoveryPublisher.RegisterScopeMatchingRule
title: IWSDiscoveryPublisher::RegisterScopeMatchingRule
author: windows-sdk-content
description: Adds support for a custom scope matching rule.
old-location: ncd\iwsdiscoverypublisher_registerscopematchingrule_method.htm
old-project: wsdapi
ms.assetid: 3ceb55de-c8be-43a7-93d7-8f674f9645ef
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: IWSDiscoveryPublisher interface,RegisterScopeMatchingRule method, IWSDiscoveryPublisher.RegisterScopeMatchingRule, IWSDiscoveryPublisher::RegisterScopeMatchingRule, RegisterScopeMatchingRule, RegisterScopeMatchingRule method, RegisterScopeMatchingRule method,IWSDiscoveryPublisher interface, ncd.iwsdiscoverypublisher_registerscopematchingrule_method, wsddisco/IWSDiscoveryPublisher::RegisterScopeMatchingRule
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
 - IWSDiscoveryPublisher.RegisterScopeMatchingRule
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryPublisher::RegisterScopeMatchingRule


## -description


Adds support for a custom scope matching rule.


## -parameters




### -param pScopeMatchingRule [in]

Pointer to an <a href="https://msdn.microsoft.com/c608215d-6c72-4567-bf81-15af665e8c52">IWSDScopeMatchingRule</a> object that represents a  custom scope matching rule.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pScopeMatchingRule</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



<b>RegisterScopeMatchingRule</b> allows custom scope matching rules to be defined and added to the existing set defined in the <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery specification</a>.




## -see-also




<a href="https://msdn.microsoft.com/4fff1328-d315-4a26-b7d8-43a273133e08">IWSDiscoveryPublisher</a>
 

 

