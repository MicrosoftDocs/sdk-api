---
UID: NF:iaccess.IAccessControl.SetOwner
title: IAccessControl::SetOwner
author: windows-sdk-content
description: Sets the owner or the group of an item.
old-location: com\iaccesscontrol_setowner.htm
tech.root: com
ms.assetid: 92406043-f4a4-43e4-9b17-087066823ce4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IAccessControl interface [COM],SetOwner method, IAccessControl.SetOwner, IAccessControl::SetOwner, SetOwner, SetOwner method [COM], SetOwner method [COM],IAccessControl interface, _com_iaccesscontrol_setowner, com.iaccesscontrol_setowner, iaccess/IAccessControl::SetOwner
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
 - IAccessControl.SetOwner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAccessControl::SetOwner


## -description


Sets the owner or the group of an item.


## -parameters




### -param pOwner [in]

The address of the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure for the owner.


### -param pGroup [in]

The address of the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure for the group.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>SetOwner</b> method is not implemented by CLSID_DCOMAccessControl.





## -see-also




<a href="https://msdn.microsoft.com/f7f19a9d-27ed-479f-b5d4-562cab5be12a">IAccessControl</a>
 

 

