---
UID: NF:shobjidl.INameSpaceTreeControl2.SetControlStyle2
title: INameSpaceTreeControl2::SetControlStyle2
author: windows-sdk-content
description: Sets the extended display styles for the namespace object's treeview controls.
old-location: shell\INameSpaceTreeControl2_SetControlStyle2.htm
tech.root: shell
ms.assetid: 17d54fa9-ff5c-4fca-a7a6-7ecd4a58c7b9
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: INameSpaceTreeControl2 interface [Windows Shell],SetControlStyle2 method, INameSpaceTreeControl2.SetControlStyle2, INameSpaceTreeControl2::SetControlStyle2, SetControlStyle2, SetControlStyle2 method [Windows Shell], SetControlStyle2 method [Windows Shell],INameSpaceTreeControl2 interface, _shell_INameSpaceTreeControl2_SetControlStyle2, shell.INameSpaceTreeControl2_SetControlStyle2, shobjidl/INameSpaceTreeControl2::SetControlStyle2
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
 - INameSpaceTreeControl2.SetControlStyle2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INameSpaceTreeControl2::SetControlStyle2


## -description


Sets the extended display styles for the namespace object's treeview controls.


## -parameters




### -param nstcsMask [in]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a></b>

One or more of the <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> constants that specify the styles for which the method should set new values.


### -param nstcsStyle [in]

Type: <b><a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a></b>

A bitmap that contains the new values for the styles specified in <i>nstcsMask</i>. If the bit that represents the individual <a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a> value is 0, that style is not used. If the value is 1, the style is applied to the treeview. Styles in positions not specified in <i>nstcsMask</i> are left at their current setting regardless of their bit's value in this bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a>



<a href="https://msdn.microsoft.com/1c96d936-2a79-491b-8e1e-2dd0e71aba10">INameSpaceTreeControl2::GetControlStyle2</a>



<a href="https://msdn.microsoft.com/20a212e2-13e8-4e17-a8d3-78fff2a1fafb">INameSpaceTreeControl2::SetControlStyle</a>



<a href="https://msdn.microsoft.com/0bfa6900-71c0-44b7-8157-662bee58e6c9">NSTCSTYLE2</a>
 

 

