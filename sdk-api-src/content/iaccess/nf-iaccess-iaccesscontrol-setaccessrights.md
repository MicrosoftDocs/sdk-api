---
UID: NF:iaccess.IAccessControl.SetAccessRights
title: IAccessControl::SetAccessRights (iaccess.h)
author: windows-sdk-content
description: Replaces the existing access rights on an object with the specified list.
old-location: com\iaccesscontrol_setaccessrights.htm
tech.root: com
ms.assetid: 5f4224fe-255f-4eb7-88bb-47501718589b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAccessControl interface [COM],SetAccessRights method, IAccessControl.SetAccessRights, IAccessControl::SetAccessRights, SetAccessRights, SetAccessRights method [COM], SetAccessRights method [COM],IAccessControl interface, _com_iaccesscontrol_setaccessrights, com.iaccesscontrol_setaccessrights, iaccess/IAccessControl::SetAccessRights
ms.topic: method
f1_keywords: 
 - "iaccess/IAccessControl.SetAccessRights"
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
 - IAccessControl.SetAccessRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAccessControl::SetAccessRights


## -description


Replaces the existing access rights on an object with the specified list.


## -parameters




### -param pAccessList [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-_actrl_alista">ACTRL_ACCESS</a> list that contains an array of access lists to be written to the object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>
 

 

