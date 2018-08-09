---
UID: NF:shobjidl.INameSpaceTreeControl2.SetControlStyle
title: INameSpaceTreeControl2::SetControlStyle
author: windows-sdk-content
description: Sets the display styles for the namespace object's treeview controls.
old-location: shell\INameSpaceTreeControl2_SetControlStyle.htm
old-project: shell
ms.assetid: 20a212e2-13e8-4e17-a8d3-78fff2a1fafb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: INameSpaceTreeControl2 interface [Windows Shell],SetControlStyle method, INameSpaceTreeControl2.SetControlStyle, INameSpaceTreeControl2::SetControlStyle, SetControlStyle, SetControlStyle method [Windows Shell], SetControlStyle method [Windows Shell],INameSpaceTreeControl2 interface, _shell_INameSpaceTreeControl2_SetControlStyle, shell.INameSpaceTreeControl2_SetControlStyle, shobjidl/INameSpaceTreeControl2::SetControlStyle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - INameSpaceTreeControl2.SetControlStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# INameSpaceTreeControl2::SetControlStyle


## -description


Sets the display styles for the namespace object's treeview controls.


## -parameters




### -param nstcsMask [in]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a></b>

One or more of the <a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a> constants that specify the styles for which the method should set new values.


### -param nstcsStyle [in]

Type: <b><a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a></b>

A bitmap that contains the new values for the styles specified in <i>nstcsMask</i>. If the bit that represents the individual <a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a> value is 0, that style is not used. If the value is 1, the style is applied to the treeview. Styles in positions not specified in <i>nstcsMask</i> are left at their current setting regardless of their bit's value in this bitmap.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5f9514db-35fe-44c7-9324-d69022628913">INameSpaceTreeControl2</a>



<a href="https://msdn.microsoft.com/5305d7ba-e37f-4f95-8ae2-e0532012cb1e">INameSpaceTreeControl2::GetControlStyle</a>



<a href="https://msdn.microsoft.com/17d54fa9-ff5c-4fca-a7a6-7ecd4a58c7b9">INameSpaceTreeControl2::SetControlStyle2</a>



<a href="https://msdn.microsoft.com/879af1be-2eea-4ebd-b9ea-64b1db40682d">NSTCSTYLE</a>
 

 

