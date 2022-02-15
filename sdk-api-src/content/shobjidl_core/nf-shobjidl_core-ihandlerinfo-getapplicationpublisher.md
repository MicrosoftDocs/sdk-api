---
UID: NF:shobjidl_core.IHandlerInfo.GetApplicationPublisher
title: IHandlerInfo::GetApplicationPublisher (shobjidl_core.h)
description: Retrieves the name of the publisher of the application that implemented the handler.
helpviewer_keywords: ["GetApplicationPublisher","GetApplicationPublisher method [Windows Shell]","GetApplicationPublisher method [Windows Shell]","IHandlerInfo interface","IHandlerInfo interface [Windows Shell]","GetApplicationPublisher method","IHandlerInfo.GetApplicationPublisher","IHandlerInfo::GetApplicationPublisher","shell.IHandlerInfo_GetApplicationPublisher","shobjidl_core/IHandlerInfo::GetApplicationPublisher"]
old-location: shell\IHandlerInfo_GetApplicationPublisher.htm
tech.root: shell
ms.assetid: d5e22afa-69eb-4cf5-98b0-f46e25fb136e
ms.date: 12/05/2018
ms.keywords: GetApplicationPublisher, GetApplicationPublisher method [Windows Shell], GetApplicationPublisher method [Windows Shell],IHandlerInfo interface, IHandlerInfo interface [Windows Shell],GetApplicationPublisher method, IHandlerInfo.GetApplicationPublisher, IHandlerInfo::GetApplicationPublisher, shell.IHandlerInfo_GetApplicationPublisher, shobjidl_core/IHandlerInfo::GetApplicationPublisher
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
 - IHandlerInfo::GetApplicationPublisher
 - shobjidl_core/IHandlerInfo::GetApplicationPublisher
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
 - IHandlerInfo.GetApplicationPublisher
---

# IHandlerInfo::GetApplicationPublisher


## -description

Retrieves the name of the publisher of the application that implemented the handler.

## -parameters

### -param value [out]

Type: <b>LPWSTR*</b>

A pointer to a string that, when this method returns successfully, receives the publisher's name.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo">IHandlerInfo</a>