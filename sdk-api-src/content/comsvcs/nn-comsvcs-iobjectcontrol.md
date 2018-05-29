---
UID: NN:comsvcs.IObjectControl
title: IObjectControl
author: windows-sdk-content
description: Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.
old-location: cos\iobjectcontrol.htm
old-project: cossdk
ms.assetid: cbc63f97-dfc7-4e1f-97f9-2043f8bea1d4
ms.author: windowssdkdev
ms.date: 05/16/2018
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IObjectControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectControl interface


## -description


Defines context-specific initialization and cleanup procedures for your COM+ objects, and specifies whether the objects can be recycled.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IObjectControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IObjectControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/53bf55a2-0cfa-4612-bca7-c6693f84e18f">Activate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform context-specific initialization whenever it is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97f585f1-e9c2-4122-a5e9-0a10b874b06e">CanBePooled</a>
</td>
<td align="left" width="63%">
Notifies the COM+ run-time environment whether the object can be pooled for reuse when it is deactivated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e076e7ce-867a-47ab-bd7e-9754b7d81e43">Deactivate</a>
</td>
<td align="left" width="63%">
Enables a COM+ object to perform required cleanup before it is recycled or destroyed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/e5602af2-5852-4c34-a792-6742e90b7d41">Context Activation</a>
 

 

