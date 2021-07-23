---
UID: NN:shobjidl_core.IExecuteCommandApplicationHostEnvironment
title: IExecuteCommandApplicationHostEnvironment (shobjidl_core.h)
description: Provides a single method that enables an application to determine whether its host is in desktop or immersive mode.
helpviewer_keywords: ["IExecuteCommandApplicationHostEnvironment","IExecuteCommandApplicationHostEnvironment interface [Windows Shell]","IExecuteCommandApplicationHostEnvironment interface [Windows Shell]","described","shell.IExecuteCommandApplicationHostEnvironment","shobjidl_core/IExecuteCommandApplicationHostEnvironment"]
old-location: shell\IExecuteCommandApplicationHostEnvironment.htm
tech.root: shell
ms.assetid: c890d306-66df-4c29-88db-d54362ac018a
ms.date: 12/05/2018
ms.keywords: IExecuteCommandApplicationHostEnvironment, IExecuteCommandApplicationHostEnvironment interface [Windows Shell], IExecuteCommandApplicationHostEnvironment interface [Windows Shell],described, shell.IExecuteCommandApplicationHostEnvironment, shobjidl_core/IExecuteCommandApplicationHostEnvironment
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
 - IExecuteCommandApplicationHostEnvironment
 - shobjidl_core/IExecuteCommandApplicationHostEnvironment
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
 - IExecuteCommandApplicationHostEnvironment
---

# IExecuteCommandApplicationHostEnvironment interface


## -description

Provides a single method that enables an application to determine whether its host is in desktop or immersive mode.

## -inheritance

The <b>IExecuteCommandApplicationHostEnvironment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExecuteCommandApplicationHostEnvironment</b> also has these types of members:

## -remarks

<h3><a id="When_to_implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to implement</h3>
An application must implement this interface together with the DelegateExecute handler (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand">IExecuteCommand</a>).
