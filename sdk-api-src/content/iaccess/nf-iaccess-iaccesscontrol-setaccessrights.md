---
UID: NF:iaccess.IAccessControl.SetAccessRights
title: IAccessControl::SetAccessRights method
author: windows-driver-content
description: Replaces the existing access rights on an object with the specified list.
old-location: com\iaccesscontrol_setaccessrights.htm
old-project: com
ms.assetid: 5f4224fe-255f-4eb7-88bb-47501718589b
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IAccessControl, IAccessControl interface [COM], SetAccessRights method, IAccessControl::SetAccessRights, SetAccessRights method [COM], SetAccessRights method [COM], IAccessControl interface, SetAccessRights,IAccessControl.SetAccessRights, _com_iaccesscontrol_setaccessrights, com.iaccesscontrol_setaccessrights, iaccess/IAccessControl::SetAccessRights
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
req.typenames: HTTP_VERSION, *PHTTP_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	IAccess.h
api_name:
-	IAccessControl.SetAccessRights
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAccessControl::SetAccessRights method


## -description


Replaces the existing access rights on an object with the specified list.


## -parameters




### -param pAccessList [in]

A pointer to the <a href="https://msdn.microsoft.com/d7fb10c1-ebb8-44cf-b61c-a70a787b324f">ACTRL_ACCESS</a> list that contains an array of access lists to be written to the object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>
 

 

