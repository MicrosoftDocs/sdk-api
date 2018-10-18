---
UID: NF:shobjidl_core.ITaskbarList4.SetTabProperties
title: ITaskbarList4::SetTabProperties
author: windows-sdk-content
description: Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.
old-location: shell\ITaskbarList4_SetTabProperties.htm
tech.root: shell
ms.assetid: cc3fec4b-7770-44af-9892-239a17dd96b8
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ITaskbarList4 interface [Windows Shell],SetTabProperties method, ITaskbarList4.SetTabProperties, ITaskbarList4::SetTabProperties, SetTabProperties, SetTabProperties method [Windows Shell], SetTabProperties method [Windows Shell],ITaskbarList4 interface, _shell_ITaskbarList4_SetTabProperties, shell.ITaskbarList4_SetTabProperties, shobjidl_core/ITaskbarList4::SetTabProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - shobjidl_core.h
api_name:
 - ITaskbarList4.SetTabProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList4::SetTabProperties


## -description


Allows a tab to specify whether the main application frame window or the tab window should be used as a thumbnail or in the peek feature under certain circumstances.


## -parameters




### -param hwndTab [in]

Type: <b>HWND</b>

The handle of the tab window that is to have properties set. This handle must already be registered through <a href="https://msdn.microsoft.com/b0cdca51-108a-4507-bd9e-6bcd4386c36a">RegisterTab</a>.


### -param stpFlags [in]

Type: <b><a href="https://msdn.microsoft.com/7d50e4fe-1689-4dbd-b367-f4881d8d5d78">STPFLAG</a></b>

One or more members of the <a href="https://msdn.microsoft.com/7d50e4fe-1689-4dbd-b367-f4881d8d5d78">STPFLAG</a> enumeration that specify the displayed thumbnail and peek image source of the tab thumbnail.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An application might want to use the thumbnail or peek representation of its associated parent window if the application cannot generate its own thumbnail for a tab or for its active tab content (such as an animation) to appear live.




## -see-also




<a href="https://msdn.microsoft.com/7fc2c615-0bb0-4c03-9775-eee566c71088">ITaskbarList4</a>
 

 

