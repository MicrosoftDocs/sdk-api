---
UID: NN:iaccess.IAccessControl
title: IAccessControl
author: windows-sdk-content
description: Enables the management of access to objects and properties on the objects.
old-location: com\iaccesscontrol.htm
tech.root: com
ms.assetid: f7f19a9d-27ed-479f-b5d4-562cab5be12a
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IAccessControl, IAccessControl interface [COM], IAccessControl interface [COM],described, _com_iaccesscontrol, com.iaccesscontrol, iaccess/IAccessControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: iaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: IAccess.idl
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
 - IAccess.h
api_name:
 - IAccessControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessControl interface


## -description


Enables the management of access to objects and properties on the objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IAccessControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAccessControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c8551fb-8ba9-4a52-b6f8-bd11e4006fe9">GetAllAccessRights</a>
</td>
<td align="left" width="63%">
Gets the entire list of access rights and/or the owner and group for the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8ec6743-633b-4c79-afac-68eb20e07b2a">GrantAccessRights</a>
</td>
<td align="left" width="63%">
Merges the new list of access rights with the existing access rights on the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee9e7e2d-caec-443c-937d-b8fc64130ad4">IsAccessAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the specified trustee has access rights to the object or property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09b37002-0ad3-43c2-8a39-b440158310bb">RevokeAccessRights</a>
</td>
<td align="left" width="63%">
Removes any explicit entries for the list of trustees.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f4224fe-255f-4eb7-88bb-47501718589b">SetAccessRights</a>
</td>
<td align="left" width="63%">
Replaces the existing access rights on an object with the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92406043-f4a4-43e4-9b17-087066823ce4">SetOwner</a>
</td>
<td align="left" width="63%">
Sets the owner or the group of an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a>



<a href="https://msdn.microsoft.com/20b66868-fb9a-489f-97a2-59a8a825c8d9">Setting Process-Wide Security with CoInitializeSecurity</a>
 

 

