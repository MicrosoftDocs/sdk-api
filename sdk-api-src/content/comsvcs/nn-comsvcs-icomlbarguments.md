---
UID: NN:comsvcs.ICOMLBArguments
title: ICOMLBArguments
author: windows-sdk-content
description: Used to activate the COM+ component load balancing service.
old-location: cos\icomlbarguments.htm
old-project: cossdk
ms.assetid: 1eb1c464-9371-420e-afc0-4b18c11a70d4
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ICOMLBArguments, ICOMLBArguments interface [COM+], ICOMLBArguments interface [COM+],described, _cos_icomlbarguments, comsvcs/ICOMLBArguments, cos.icomlbarguments
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
 - ICOMLBArguments
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMLBArguments interface


## -description


Used to activate the COM+ component load balancing service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMLBArguments</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICOMLBArguments</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICOMLBArguments</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0475bd9e-dcde-47e4-b9e4-bcaa6d0ad919">GetCLSID</a>
</td>
<td align="left" width="63%">
Retrieves the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1f6adc8-2e89-4f64-9694-2342c967a142">GetMachineName</a>
</td>
<td align="left" width="63%">
Retrieves the computer name for the load balancing server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f24611-0f98-4226-858b-90fef35cc257">SetCLSID</a>
</td>
<td align="left" width="63%">
Sets the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55f9d45e-5c36-4f02-9a9d-111ad4abf016">SetMachineName</a>
</td>
<td align="left" width="63%">
Sets the computer name for the load balancing server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ce2edece-6375-4101-b288-c250fb21cfb7">ISelectCOMLBServer</a>
 

 

