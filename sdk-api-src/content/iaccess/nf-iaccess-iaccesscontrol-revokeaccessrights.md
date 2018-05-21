---
UID: NF:iaccess.IAccessControl.RevokeAccessRights
title: IAccessControl::RevokeAccessRights
author: windows-driver-content
description: Removes any explicit entries for the list of trustees.
old-location: com\iaccesscontrol_revokeaccessrights.htm
old-project: com
ms.assetid: 09b37002-0ad3-43c2-8a39-b440158310bb
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAccessControl interface [COM],RevokeAccessRights method, IAccessControl.RevokeAccessRights, IAccessControl::RevokeAccessRights, RevokeAccessRights, RevokeAccessRights method [COM], RevokeAccessRights method [COM],IAccessControl interface, _com_iaccesscontrol_revokeaccessrights, com.iaccesscontrol_revokeaccessrights, iaccess/IAccessControl::RevokeAccessRights
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
-	IAccessControl.RevokeAccessRights
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAccessControl::RevokeAccessRights


## -description


Removes any explicit entries for the list of trustees.


## -parameters




### -param lpProperty [in]

The name of the property. If you are using the COM implementation of <a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>, this parameter must be <b>NULL</b>.


### -param cTrustees [in]

The number of trustees in the list. This parameter cannot be 0. 


### -param prgTrustees [in]

A pointer to an array of trustee names. See <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Even after removing explicit entries, the trustees might still have access entries due to group inclusion.




## -see-also




<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>
 

 

