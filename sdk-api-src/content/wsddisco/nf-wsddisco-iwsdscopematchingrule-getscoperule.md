---
UID: NF:wsddisco.IWSDScopeMatchingRule.GetScopeRule
title: IWSDScopeMatchingRule::GetScopeRule
author: windows-sdk-content
description: Is called to return a URI defining the implemented scope matching rule.
old-location: ncd\iwsdscopematchingrule_getscoperule_method.htm
tech.root: wsdapi
ms.assetid: 86ce14eb-555f-4575-a335-8a428cffa20d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetScopeRule, GetScopeRule method, GetScopeRule method,IWSDScopeMatchingRule interface, IWSDScopeMatchingRule interface,GetScopeRule method, IWSDScopeMatchingRule.GetScopeRule, IWSDScopeMatchingRule::GetScopeRule, ncd.iwsdscopematchingrule_getscoperule_method, wsddisco/IWSDScopeMatchingRule::GetScopeRule
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
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDScopeMatchingRule.GetScopeRule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDScopeMatchingRule::GetScopeRule


## -description


Is called to return a URI defining the implemented scope matching rule.


## -parameters




### -param ppszScopeMatchingRule [out]

Pointer to the scope matching rule. The implementor must allocate memory using <a href="https://msdn.microsoft.com/2608985f-56aa-4223-b76d-85ebe3b080fb">WSDAllocateLinkedMemory</a> and the caller must release memory using <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.


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
</table>
 




## -remarks



<b>GetScopeRule</b> should provide a copy of the URI for the scope matching rule this object represents. The copy will be released by the caller using <a href="https://msdn.microsoft.com/8fe6f586-a262-4248-9650-dec0fae8cd74">WSDFreeLinkedMemory</a>.

<i>ppszScopeMatchingRule</i> should never be <b>NULL</b> or an empty string. To register for the <b>NULL</b> scope matching rule, register for the RFC2396 rule as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a>. Probe messages containing a <b>NULL</b> MatchBy value will be converted to RFC2396 before <b>GetScopeRule</b> is called.




## -see-also




<a href="https://msdn.microsoft.com/c608215d-6c72-4567-bf81-15af665e8c52">IWSDScopeMatchingRule</a>
 

 

