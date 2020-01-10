---
UID: NN:mergemod.IMsmDependency
title: IMsmDependency (mergemod.h)
description: The IMsmDependency interface retrieves details for a single module dependency.
old-location: setup\imsmdependency_interface.htm
tech.root: Msi
ms.assetid: 517cf174-418a-4717-a25f-1736225016a1
ms.date: 12/05/2018
ms.keywords: IMsmDependency, IMsmDependency interface, IMsmDependency interface,described, mergemod/IMsmDependency, setup.imsmdependency_interface
f1_keywords:
- mergemod/IMsmDependency
dev_langs:
- c++
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
req.target-min-winversvr: 
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
req.dll: Mergemod.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mergemod.dll
api_name:
- IMsmDependency
- IMsmDependency.get_Module
- IMsmDependency.get_Language
- IMsmDependency.get_Version
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMsmDependency interface


## -description


The <b>IMsmDependency</b> interface retrieves details for a single module 
dependency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMsmDependency</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMsmDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Language</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-language">Language</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-object">Dependency</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Module</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-module">Module</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-object">Dependency</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>get_Version</b></td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-version">Version</a> property of the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/dependency-object">Dependency</a> object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>
 

 

