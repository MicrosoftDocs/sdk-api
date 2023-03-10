---
UID: NN:shobjidl_core.IInitializeWithWindow
title: IInitializeWithWindow (shobjidl_core.h)
description: Exposes a method through which a client can provide an owner window to a Windows Runtime object used in a desktop application.
helpviewer_keywords: ["IInitializeWithWindow","IInitializeWithWindow interface [Windows Shell]","IInitializeWithWindow interface [Windows Shell]","described","shell.IInitializeWithWindow","shobjidl_core/IInitializeWithWindow"]
old-location: shell\IInitializeWithWindow.htm
tech.root: shell
ms.assetid: 8421BFA0-0655-447c-99BB-3D4F049C572D
ms.date: 12/05/2018
ms.keywords: IInitializeWithWindow, IInitializeWithWindow interface [Windows Shell], IInitializeWithWindow interface [Windows Shell],described, shell.IInitializeWithWindow, shobjidl_core/IInitializeWithWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInitializeWithWindow
 - shobjidl_core/IInitializeWithWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IInitializeWithWindow
---

## -description

Exposes a method through which a client can provide an owner window to a Windows Runtime (WinRT) object used in a desktop application.

For info and code examples about this interface, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects). In addition to the types listed in that topic, [**Shell data object**](/windows/win32/shell/dataobject) is also associated with this API.

## -inheritance

The **IInitializeWithWindow** interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithWindow</b> also has these types of members:

## -remarks

Implement this interface if your object needs to be provided with an owner window, generally to display UI. Most third-party applications will not need to implement this interface.

## -see-also

* [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects)
