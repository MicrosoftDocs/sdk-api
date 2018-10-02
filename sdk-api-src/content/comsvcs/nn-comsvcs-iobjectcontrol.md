---
UID: NN:comsvcs.IObjectControl
title: IObjectControl
author: windows-sdk-content
description: Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.
old-location: cos\iobjectcontrol.htm
tech.root: cossdk
ms.assetid: cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IObjectControl, IObjectControl interface [COM+], IObjectControl interface [COM+],described, _cos_IObjectControl, comsvcs/IObjectControl, cos.iobjectcontrol
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
 - IObjectControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectControl interface


## -description


Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IObjectControl</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IObjectControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681303(v=VS.85).aspx">Activate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform context-specific initialization whenever it is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684322(v=VS.85).aspx">CanBePooled</a>
</td>
<td align="left" width="63%">
Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687094(v=VS.85).aspx">Deactivate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform required cleanup before it is recycled or destroyed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687581(v=VS.85).aspx">Context Activation</a>
 

 

