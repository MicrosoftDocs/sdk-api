---
UID: NN:comsvcs.ICOMLBArguments
title: ICOMLBArguments
author: windows-sdk-content
description: Used to activate the COM+ component load balancing service.
old-location: cos\icomlbarguments.htm
tech.root: cossdk
ms.assetid: 1eb1c464-9371-420e-afc0-4b18c11a70d4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICOMLBArguments, ICOMLBArguments interface [COM+], ICOMLBArguments interface [COM+],described, _cos_icomlbarguments, comsvcs/ICOMLBArguments, cos.icomlbarguments
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICOMLBArguments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMLBArguments interface


## -description


Used to activate the COM+ component load balancing service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMLBArguments</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ICOMLBArguments</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms678866(v=VS.85).aspx">GetCLSID</a>
</td>
<td align="left" width="63%">
Retrieves the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685973(v=VS.85).aspx">GetMachineName</a>
</td>
<td align="left" width="63%">
Retrieves the computer name for the load balancing server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681808(v=VS.85).aspx">SetCLSID</a>
</td>
<td align="left" width="63%">
Sets the object's CLSID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681313(v=VS.85).aspx">SetMachineName</a>
</td>
<td align="left" width="63%">
Sets the computer name for the load balancing server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686509(v=VS.85).aspx">ISelectCOMLBServer</a>
 

 

