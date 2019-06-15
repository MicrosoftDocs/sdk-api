---
UID: NN:comsvcs.IGetSecurityCallContext
title: IGetSecurityCallContext (comsvcs.h)
author: windows-sdk-content
description: Retrieves a reference to an object created from the SecurityCallContext class that is associated with the current call.
old-location: cos\igetsecuritycallcontext.htm
tech.root: cossdk
ms.assetid: 7be988b7-b144-4b8f-b8d3-b0700b564df3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IGetSecurityCallContext, IGetSecurityCallContext interface [COM+], IGetSecurityCallContext interface [COM+],described, _cos_IGetSecurityCallContext, comsvcs/IGetSecurityCallContext, cos.igetsecuritycallcontext
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IGetSecurityCallContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGetSecurityCallContext interface


## -description


Retrieves a reference to an object created from the <a href="https://docs.microsoft.com/windows/desktop/cossdk/securitycallcontext">SecurityCallContext</a> class that is associated with the current call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGetSecurityCallContext</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGetSecurityCallContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGetSecurityCallContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext">GetSecurityClassContext</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an object created from the <a href="https://docs.microsoft.com/windows/desktop/cossdk/securitycallcontext">SecurityCallContext</a> class that is associated with the current call.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext">CoGetCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/securitycallcontext">SecurityCallContext</a>
 

 

