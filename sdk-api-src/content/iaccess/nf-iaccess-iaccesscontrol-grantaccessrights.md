---
UID: NF:iaccess.IAccessControl.GrantAccessRights
title: IAccessControl::GrantAccessRights method
author: windows-driver-content
description: Merges the new list of access rights with the existing access rights on the object.
old-location: com\iaccesscontrol_grantaccessrights.htm
old-project: com
ms.assetid: f8ec6743-633b-4c79-afac-68eb20e07b2a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GrantAccessRights method [COM], GrantAccessRights method [COM], IAccessControl interface, GrantAccessRights,IAccessControl.GrantAccessRights, IAccessControl, IAccessControl interface [COM], GrantAccessRights method, IAccessControl::GrantAccessRights, _com_iaccesscontrol_grantaccessrights, com.iaccesscontrol_grantaccessrights, iaccess/IAccessControl::GrantAccessRights
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: HTTP_FILTER_VERSION, *PHTTP_FILTER_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	IAccess.h
api_name:
-	IAccessControl.GrantAccessRights
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAccessControl::GrantAccessRights method


## -description


Merges the new list of access rights with the existing access rights on the object.


## -parameters




### -param pAccessList [in]

A pointer to the <a href="https://msdn.microsoft.com/d7fb10c1-ebb8-44cf-b61c-a70a787b324f">ACTRL_ACCESS</a> structure that contains an array of access lists for the object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Merging the new access rights list with the existing access rights ensures that the object will have at least the indicated access rights. This merge process consists of adding the new denied access rights before the old denied access rights, and the new allowed access rights before the existing allowed rights. None of the existing rights are removed.

Following a merge, the access rights on an object are ordered as follows:

<ol>
<li>[New Access Denied]</li>
<li>[Old Access Denied]</li>
<li>[New Access Allowed]</li>
<li>[Old Access Allowed]</li>
</ol>
The system-supplied implementation of <b>GrantAccessRights</b> (CLSID_DCOMAccessControl) requires that the <b>cEntries</b> member of the <a href="https://msdn.microsoft.com/d7fb10c1-ebb8-44cf-b61c-a70a787b324f">ACTRL_ACCESSW</a> structure be set to 1. In addition, the <b>lpProperty</b> member of the <a href="https://msdn.microsoft.com/90b13dd1-0ca6-4674-b9fa-a61aed4637d7">ACTRL_PROPERTY_ENTRYW</a> structure must be <b>NULL</b> to indicate that the access entry list applies to the object itself.




## -see-also




<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>
 

 

