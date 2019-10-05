---
UID: NN:comsvcs.ISharedPropertyGroupManager
title: ISharedPropertyGroupManager (comsvcs.h)
author: windows-sdk-content
description: Used to create shared property groups and to obtain access to existing shared property groups.
old-location: cos\isharedpropertygroupmanager.htm
tech.root: cossdk
ms.assetid: 71c0a1de-5ea5-4496-b0e9-56d0cc8129a9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISharedPropertyGroupManager, ISharedPropertyGroupManager interface [COM+], ISharedPropertyGroupManager interface [COM+],described, _cos_ISharedPropertyGroupManager, comsvcs/ISharedPropertyGroupManager, cos.isharedpropertygroupmanager
ms.topic: interface
f1_keywords: 
 - "comsvcs/ISharedPropertyGroupManager"
dev_langs:
 - c++
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
 - ISharedPropertyGroupManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharedPropertyGroupManager interface


## -description


Used to create shared property groups and to obtain access to existing shared property groups.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedPropertyGroupManager</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISharedPropertyGroupManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedPropertyGroupManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup">CreatePropertyGroup</a>
</td>
<td align="left" width="63%">
Creates a new shared property group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroupmanager-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the named security call context properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-isharedpropertygroupmanager-get_group">get_Group</a>
</td>
<td align="left" width="63%">
Retrieves a reference to an existing shared property group.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isharedproperty">ISharedProperty</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-isharedpropertygroup">ISharedPropertyGroup</a>
 

 

