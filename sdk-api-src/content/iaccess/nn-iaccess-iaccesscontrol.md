---
UID: NN:iaccess.IAccessControl
title: IAccessControl (iaccess.h)
description: Enables the management of access to objects and properties on the objects.
helpviewer_keywords: ["IAccessControl","IAccessControl interface [COM]","IAccessControl interface [COM]","described","_com_iaccesscontrol","com.iaccesscontrol","iaccess/IAccessControl"]
old-location: com\iaccesscontrol.htm
tech.root: com
ms.assetid: f7f19a9d-27ed-479f-b5d4-562cab5be12a
ms.date: 12/05/2018
ms.keywords: IAccessControl, IAccessControl interface [COM], IAccessControl interface [COM],described, _com_iaccesscontrol, com.iaccesscontrol, iaccess/IAccessControl
f1_keywords:
- iaccess/IAccessControl
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessControl interface


## -description


Enables the management of access to objects and properties on the objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAccessControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-getallaccessrights">GetAllAccessRights</a>
</td>
<td align="left" width="63%">
Gets the entire list of access rights and/or the owner and group for the specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-grantaccessrights">GrantAccessRights</a>
</td>
<td align="left" width="63%">
Merges the new list of access rights with the existing access rights on the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-isaccessallowed">IsAccessAllowed</a>
</td>
<td align="left" width="63%">
Determines whether the specified trustee has access rights to the object or property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-revokeaccessrights">RevokeAccessRights</a>
</td>
<td align="left" width="63%">
Removes any explicit entries for the list of trustees.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-setaccessrights">SetAccessRights</a>
</td>
<td align="left" width="63%">
Replaces the existing access rights on an object with the specified list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nf-iaccess-iaccesscontrol-setowner">SetOwner</a>
</td>
<td align="left" width="63%">
Sets the owner or the group of an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a>



<a href="https://docs.microsoft.com/windows/desktop/com/setting-processwide-security-with-coinitializesecurity">Setting Process-Wide Security with CoInitializeSecurity</a>
 

 

