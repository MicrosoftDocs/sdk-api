---
UID: NN:shobjidl_core.IPackageExecutionStateChangeNotification
title: IPackageExecutionStateChangeNotification (shobjidl_core.h)
description: Enables receiving package state-change notifications during Windows Store app debugging.
helpviewer_keywords: ["IPackageExecutionStateChangeNotification","IPackageExecutionStateChangeNotification interface [Windows Shell]","IPackageExecutionStateChangeNotification interface [Windows Shell]","described","shell.IPackageExecutionStateChangeNotification","shobjidl_core/IPackageExecutionStateChangeNotification"]
old-location: shell\IPackageExecutionStateChangeNotification.htm
tech.root: shell
ms.assetid: 6AD9A9CD-933B-432F-A124-48092588C5DF
ms.date: 12/05/2018
ms.keywords: IPackageExecutionStateChangeNotification, IPackageExecutionStateChangeNotification interface [Windows Shell], IPackageExecutionStateChangeNotification interface [Windows Shell],described, shell.IPackageExecutionStateChangeNotification, shobjidl_core/IPackageExecutionStateChangeNotification
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
 - IPackageExecutionStateChangeNotification
 - shobjidl_core/IPackageExecutionStateChangeNotification
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
 - IPackageExecutionStateChangeNotification
---

# IPackageExecutionStateChangeNotification interface


## -description

Enables receiving package state-change notifications during Windows Store app debugging.

## -inheritance

The <b>IPackageExecutionStateChangeNotification</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPackageExecutionStateChangeNotification</b> also has these types of members:

## -remarks

Implement the <b>IPackageExecutionStateChangeNotification</b> interface when you need to receive package state-change notifications during Windows Store app debugging. 

Call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a> method to register for package state-change notifications.

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>
