---
UID: NL:methodco.MethodContext
title: MethodContext (methodco.h)
description: The MethodContext class is the pointer to a structure used in a provider to get or set IWbemClassObject information. WMI does not implement any functionality based on the pointer.helpviewer_keywords: ["MethodContext","MethodContext class [Windows Management Instrumentation]","MethodContext class [Windows Management Instrumentation]","described","methodco/MethodContext","wmi.methodcontext"]
old-location: wmi\methodcontext.htm
tech.root: WmiSdk
ms.assetid: aea20c9d-4042-426a-abdf-51ebddf017aa
ms.date: 12/05/2018
ms.keywords: MethodContext, MethodContext class [Windows Management Instrumentation], MethodContext class [Windows Management Instrumentation],described, methodco/MethodContext, wmi.methodcontext
f1_keywords:
- methodco/MethodContext
dev_langs:
- c++
req.header: methodco.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
- MethodCo.h
api_name:
- MethodContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MethodContext class


## -description


<p class="CCE_Message">[The <b>MethodContext</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure">MI APIs</a> should be used for all new 
    development.]

The <b>MethodContext</b> class is the pointer to a structure used in a provider to get or set <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">MethodContext</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="methods"></a>Methods</h3>The <b>MethodContext</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/methodco/nf-methodco-methodcontext-getstatusobject">GetStatusObject</a>
</td>
<td align="left" width="63%">
Gets an internal pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/methodco/nf-methodco-methodcontext-setstatusobject">SetStatusObject</a>
</td>
<td align="left" width="63%">
Sets an internal pointer to <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> information. WMI does not implement any functionality based on the pointer.

</td>
</tr>
</table> 


## -remarks



The destructor for this class is <b>MethodContext::~MethodContext</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/provider-framework-utility-classes">Provider Framework Utility Classes</a>
 

 

