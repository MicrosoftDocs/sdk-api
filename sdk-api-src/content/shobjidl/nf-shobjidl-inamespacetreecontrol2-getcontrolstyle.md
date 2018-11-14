---
UID: NF:shobjidl.INameSpaceTreeControl2.GetControlStyle
title: INameSpaceTreeControl2::GetControlStyle
author: windows-sdk-content
description: Gets the display styles set for the namespace object's treeview controls.
old-location: shell\INameSpaceTreeControl2_GetControlStyle.htm
tech.root: shell
ms.assetid: 5305d7ba-e37f-4f95-8ae2-e0532012cb1e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetControlStyle, GetControlStyle method [Windows Shell], GetControlStyle method [Windows Shell],INameSpaceTreeControl2 interface, INameSpaceTreeControl2 interface [Windows Shell],GetControlStyle method, INameSpaceTreeControl2.GetControlStyle, INameSpaceTreeControl2::GetControlStyle, _shell_INameSpaceTreeControl2_GetControlStyle, shell.INameSpaceTreeControl2_GetControlStyle, shobjidl/INameSpaceTreeControl2::GetControlStyle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - Shobjidl.h
api_name:
 - INameSpaceTreeControl2.GetControlStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl.h
: 
- INameSpaceTreeControl2.GetControlStyle
: 
---

# INameSpaceTreeControl2::GetControlStyle


## -description


Gets the display styles set for the namespace object's treeview controls.


## -parameters




### -param nstcsMask [in]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a></b>

One or more of the <a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a> constants that specify the values for which the method should retrieve the current settings.


### -param pnstcsStyle [out]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a>*</b>

Pointer to a value that, when this method returns successfully, receives the values requested in <i>nstcsMask</i>. If the bit that represents the individual <a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a> value is 0, that value is not set. If the value is 1, it is the current setting. Bit values in positions not specifically requested in <i>nstcsMask</i> do not necessarily reflect the current settings and should not be used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a>



<a href="https://msdn.microsoft.com/1c96d936-2a79-491b-8e1e-2dd0e71aba10">INameSpaceTreeControl2::GetControlStyle2</a>



<a href="https://msdn.microsoft.com/20a212e2-13e8-4e17-a8d3-78fff2a1fafb">INameSpaceTreeControl2::SetControlStyle</a>



<a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a>
 

 

