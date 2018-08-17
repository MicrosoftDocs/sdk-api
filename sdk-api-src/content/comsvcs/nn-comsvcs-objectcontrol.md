---
UID: NN:comsvcs.ObjectControl
title: ObjectControl
author: windows-sdk-content
description: If you implement this interface in your component, the COM+ run-time environment automatically calls its methods on your objects at the appropriate times.
old-location: cos\objectcontrol.htm
old-project: cossdk
ms.assetid: 3ca939de-31ce-4ce6-84cd-4b4191a0753c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ObjectControl, ObjectControl interface [COM+], ObjectControl interface [COM+],described, _cos_ObjectControl, comsvcs/ObjectControl, cos.objectcontrol
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
 - ObjectControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ObjectControl interface


## -description


If you implement this interface in your component, the COM+ run-time environment automatically calls its methods on your objects at the appropriate times. Only the COM+ run-time environment can invoke the <b>ObjectControl</b> methods; they are not accessible to an object's clients or to the object itself. If a client queries for the <b>ObjectControl</b> interface, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> returns E_NOINTERFACE.

<b>ObjectControl</b> and <a href="https://msdn.microsoft.com/en-us/library/ms686474(v=VS.85).aspx">IObjectControl</a> provide the same functionality, but unlike <b>IObjectControl</b>, <b>ObjectControl</b> is compatible with Automation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ObjectControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ObjectControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ObjectControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70b260e7-a51d-4ddc-b395-5478e368e776">Activate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform context-specific initialization whenever it is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679218(v=VS.85).aspx">CanBePooled</a>
</td>
<td align="left" width="63%">
Indicates whether the object can be pooled for reuse when it is deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683592(v=VS.85).aspx">Deactivate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform cleanup required before it is recycled or destroyed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687581(v=VS.85).aspx">Context Activation</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686474(v=VS.85).aspx">IObjectControl</a>
 

 

