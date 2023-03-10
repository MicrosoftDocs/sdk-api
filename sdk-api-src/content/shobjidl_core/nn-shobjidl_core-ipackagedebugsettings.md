---
UID: NN:shobjidl_core.IPackageDebugSettings
title: IPackageDebugSettings (shobjidl_core.h)
description: Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.
helpviewer_keywords: ["IPackageDebugSettings","IPackageDebugSettings interface [Windows Shell]","IPackageDebugSettings interface [Windows Shell]","described","shell.IPackageDebugSettings","shobjidl_core/IPackageDebugSettings"]
old-location: shell\IPackageDebugSettings.htm
tech.root: shell
ms.assetid: e407c4ca-0de1-4b17-bb83-5c4128952d48
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Shell], IPackageDebugSettings interface [Windows Shell],described, shell.IPackageDebugSettings, shobjidl_core/IPackageDebugSettings
req.header: shobjidl_core.h
req.include-header: 
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
 - IPackageDebugSettings
 - shobjidl_core/IPackageDebugSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings
---

# IPackageDebugSettings interface


## -description

Enables debugger developers to control the life cycle of a Windows Store app, such as suspending or resuming.

## -inheritance

The <b>IPackageDebugSettings</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPackageDebugSettings</b> also has these types of members:

## -remarks

Any debug options set remain in effect until they are cleared or this interface is released.

For debug settings to take effect on Internet Explorer in the new Windows UI, use "DefaultBrowser_NOPUBLISHERID" as the <i>packageFullName</i> parameter  for  <a href="/previous-versions/hh438393(v=vs.85)">IPackageDebugSettings</a> methods.
