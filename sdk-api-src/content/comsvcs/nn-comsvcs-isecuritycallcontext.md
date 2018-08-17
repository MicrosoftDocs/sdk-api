---
UID: NN:comsvcs.ISecurityCallContext
title: ISecurityCallContext
author: windows-sdk-content
description: Provides access to security methods and information about the security call context of the current call.
old-location: cos\isecuritycallcontext.htm
old-project: cossdk
ms.assetid: cd96ef31-784f-40fa-beb5-92a88823326b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISecurityCallContext, ISecurityCallContext interface [COM+], ISecurityCallContext interface [COM+],described, _cos_ISecurityCallContext, comsvcs/ISecurityCallContext, cos.isecuritycallcontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ISecurityCallContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISecurityCallContext interface


## -description


Provides access to security methods and information about the security call context of the current call. COM+ applications that use role-based security have access to the security call context property collection through this interface. You can obtain information about any caller in the chain of callers, as well as methods specific to COM+ role-based security. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms681779(v=VS.85).aspx">Programmatic Component Security</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISecurityCallContext</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ISecurityCallContext</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ISecurityCallContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686037(v=VS.85).aspx">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685205(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties in the security context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687599(v=VS.85).aspx">get_Item</a>
</td>
<td align="left" width="63%">
Retrieves a specified property in the security call context collection.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681305(v=VS.85).aspx">IsCallerInRole</a>
</td>
<td align="left" width="63%">
Determines whether the direct caller is in the specified role.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685980(v=VS.85).aspx">IsSecurityEnabled</a>
</td>
<td align="left" width="63%">
Determines whether security is enabled for the object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685187(v=VS.85).aspx">IsUserInRole</a>
</td>
<td align="left" width="63%">
Determines whether the specified user is in the specified role. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691483(v=VS.85).aspx">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686075(v=VS.85).aspx">ISecurityCallersColl</a>



<a href="https://msdn.microsoft.com/en-us/library/ms682165(v=VS.85).aspx">ISecurityIdentityColl</a>
 

 

