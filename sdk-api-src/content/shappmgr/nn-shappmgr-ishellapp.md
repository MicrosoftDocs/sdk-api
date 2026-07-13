---
UID: NN:shappmgr.IShellApp
title: IShellApp (shappmgr.h)
description: Exposes methods that provide general information about an application to the Add/Remove Programs Application.
helpviewer_keywords: ["IShellApp","IShellApp interface [Windows Shell]","IShellApp interface [Windows Shell]","described","inet_IShellApp","shappmgr/IShellApp","shell.IShellApp"]
old-location: shell\IShellApp.htm
tech.root: shell
ms.assetid: 2f56744c-a10e-423f-8b8f-c3257e560310
ms.date: 12/05/2018
ms.keywords: IShellApp, IShellApp interface [Windows Shell], IShellApp interface [Windows Shell],described, inet_IShellApp, shappmgr/IShellApp, shell.IShellApp
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellApp
 - shappmgr/IShellApp
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
 - IShellApp
---

# IShellApp interface


## -description

Exposes methods that provide general information about an application to the Add/Remove Programs Application. You cannot use it outside the Add/Remove Programs application. The information given by this interface includes a list of supported management actions and whether the application is currently installed.

## -inheritance

The <b>IShellApp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellApp</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>
