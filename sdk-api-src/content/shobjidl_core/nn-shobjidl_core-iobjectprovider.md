---
UID: NN:shobjidl_core.IObjectProvider
title: IObjectProvider (shobjidl_core.h)
description: Exposes a method to discover objects that are named with a GUID from another object. Unlike QueryService this interface will not delegate its functionality on to other objects.
helpviewer_keywords: ["IObjectProvider","IObjectProvider interface [Windows Shell]","IObjectProvider interface [Windows Shell]","described","_shell_IObjectProvider","shell.IObjectProvider","shobjidl_core/IObjectProvider"]
old-location: shell\IObjectProvider.htm
tech.root: shell
ms.assetid: 477991e5-0882-475c-9178-c3add695dc2c
ms.date: 12/05/2018
ms.keywords: IObjectProvider, IObjectProvider interface [Windows Shell], IObjectProvider interface [Windows Shell],described, _shell_IObjectProvider, shell.IObjectProvider, shobjidl_core/IObjectProvider
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IObjectProvider
 - shobjidl_core/IObjectProvider
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
 - IObjectProvider
---

# IObjectProvider interface


## -description

Exposes a method to discover objects that are named with a <b>GUID</b> from another object. Unlike <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> this interface will not delegate its functionality on to other objects.

## -inheritance

The <b>IObjectProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectProvider</b> also has these types of members:

## -remarks

Similar to <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a>, except that this method does not imply that unhandled or unknown requests should be forwarded.
