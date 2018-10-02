---
UID: NN:comsvcs.IComSecurityEvents
title: IComSecurityEvents
author: windows-sdk-content
description: Notifies the subscriber if the authentication of a method call succeeded or failed.
old-location: cos\icomsecurityevents.htm
tech.root: cossdk
ms.assetid: 83366f18-8dd4-4c3d-8362-4fbcc4c33b95
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComSecurityEvents, IComSecurityEvents interface [COM+], IComSecurityEvents interface [COM+],described, _dtc_IComSecurityEvents, comsvcs/IComSecurityEvents, cos.icomsecurityevents
ms.prod: windows
ms.technology: windows-sdk
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
 - IComSecurityEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComSecurityEvents interface


## -description


Notifies the subscriber if the authentication of a method call succeeded or failed. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComSecurityEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComSecurityEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IComSecurityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681240(v=VS.85).aspx">OnAuthenticate</a>
</td>
<td align="left" width="63%">
Generated when a method call level authentication succeeds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ee309565(v=VS.85).aspx">OnAuthenticateFail</a>
</td>
<td align="left" width="63%">
Generated when a method call level authentication fails.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

