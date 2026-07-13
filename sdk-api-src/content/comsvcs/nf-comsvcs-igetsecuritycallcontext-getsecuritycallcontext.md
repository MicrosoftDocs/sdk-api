---
UID: NF:comsvcs.IGetSecurityCallContext.GetSecurityCallContext
title: IGetSecurityCallContext::GetSecurityCallContext (comsvcs.h)
description: Retrieves a reference to an object created from the SecurityCallContext class that is associated with the current call. (IGetSecurityCallContext.GetSecurityCallContext)
helpviewer_keywords: ["GetSecurityCallContext","GetSecurityCallContext method [COM+]","GetSecurityCallContext method [COM+]","IGetSecurityCallContext interface","IGetSecurityCallContext interface [COM+]","GetSecurityCallContext method","IGetSecurityCallContext.GetSecurityCallContext","IGetSecurityCallContext::GetSecurityCallContext","_cos_IGetSecurityCallContext_GetSecurityCallContext","comsvcs/IGetSecurityCallContext::GetSecurityCallContext","cos.igetsecuritycallcontext_getsecuritycallcontext"]
old-location: cos\igetsecuritycallcontext_getsecuritycallcontext.htm
tech.root: cos
ms.assetid: 6a386cf6-1f75-4915-8c89-e453c4ebdab8
ms.date: 12/05/2018
ms.keywords: GetSecurityCallContext, GetSecurityCallContext method [COM+], GetSecurityCallContext method [COM+],IGetSecurityCallContext interface, IGetSecurityCallContext interface [COM+],GetSecurityCallContext method, IGetSecurityCallContext.GetSecurityCallContext, IGetSecurityCallContext::GetSecurityCallContext, _cos_IGetSecurityCallContext_GetSecurityCallContext, comsvcs/IGetSecurityCallContext::GetSecurityCallContext, cos.igetsecuritycallcontext_getsecuritycallcontext
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGetSecurityCallContext::GetSecurityCallContext
 - comsvcs/IGetSecurityCallContext::GetSecurityCallContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetSecurityCallContext.GetSecurityCallContext
---

# IGetSecurityCallContext::GetSecurityCallContext


## -description

Retrieves a reference to an object created from the <a href="/windows/desktop/cossdk/securitycallcontext">SecurityCallContext</a> class that is associated with the current call.

Instead of using this method, C++ developers should use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a> function, supplying IID_ISecurityCallContext for the <i>riid</i> parameter.

## -parameters

### -param ppObject [out]

A reference to <a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a> on the object's context.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

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
<dt><b>CONTEXT_E_NOCONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The current object does not have a context associated with it because either the component wasn't imported into an application or the object was not created with one of the COM+ CreateInstance methods. This error is also returned if the GetObjectContext method was called from a constructor or from an IUnknown method.

</td>
</tr>
</table>

## -remarks

With an object's security call context, you can retrieve items in the security call context collection, such as the minimum authentication level, the direct caller, the original caller, the chain of callers, and the number of callers. You can also call the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-issecurityenabled">IsSecurityEnabled</a> and <a href="/windows/desktop/api/comsvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole">IsCallerInRole</a> methods to ensure that a particular section of code is executed. However, you can call these methods only if role-based security is enabled and if the direct caller is a member of a specified role.

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-igetsecuritycallcontext">IGetSecurityCallContext</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>
