---
UID: NN:shlobj_core.IShellDetails
title: IShellDetails (shlobj_core.h)
description: Exposed by Shell folders to provide detailed information about the items in a folder.
helpviewer_keywords: ["IShellDetails","IShellDetails interface [Windows Shell]","IShellDetails interface [Windows Shell]","described","_win32_IShellDetails","shell.IShellDetails","shlobj_core/IShellDetails"]
old-location: shell\IShellDetails.htm
tech.root: shell
ms.assetid: c31409fd-9350-46bb-a8a0-85d5958c6e49
ms.date: 12/05/2018
ms.keywords: IShellDetails, IShellDetails interface [Windows Shell], IShellDetails interface [Windows Shell],described, _win32_IShellDetails, shell.IShellDetails, shlobj_core/IShellDetails
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellDetails
 - shlobj_core/IShellDetails
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellDetails
---

# IShellDetails interface


## -description

Exposed by Shell folders to provide detailed information about the items in a folder. This is the same information that is displayed by the Windows Explorer when the view of the folder is set to Details. For Windows 2000 and later systems, <b>IShellDetails</b> is superseded by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a>.

## -inheritance

The <b>IShellDetails</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellDetails</b> also has these types of members:

## -remarks

For Windows 2000 and later systems, folder objects should implement <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2">IShellFolder2</a> instead of this interface. However, if your application needs to function on earlier systems, <b>IShellDetails</b> should also be exposed.
