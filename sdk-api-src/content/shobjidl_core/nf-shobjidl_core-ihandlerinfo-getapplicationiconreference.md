---
UID: NF:shobjidl_core.IHandlerInfo.GetApplicationIconReference
title: IHandlerInfo::GetApplicationIconReference (shobjidl_core.h)
description: Retrieves the icon of the application that implemented the handler.helpviewer_keywords: ["GetApplicationIconReference","GetApplicationIconReference method [Windows Shell]","GetApplicationIconReference method [Windows Shell]","IHandlerInfo interface","IHandlerInfo interface [Windows Shell]","GetApplicationIconReference method","IHandlerInfo.GetApplicationIconReference","IHandlerInfo::GetApplicationIconReference","shell.IHandlerInfo_GetApplicationIconReference","shobjidl_core/IHandlerInfo::GetApplicationIconReference"]
old-location: shell\IHandlerInfo_GetApplicationIconReference.htm
tech.root: shell
ms.assetid: be886508-16a5-4a77-9fa4-b6a8d028c9e9
ms.date: 12/05/2018
ms.keywords: GetApplicationIconReference, GetApplicationIconReference method [Windows Shell], GetApplicationIconReference method [Windows Shell],IHandlerInfo interface, IHandlerInfo interface [Windows Shell],GetApplicationIconReference method, IHandlerInfo.GetApplicationIconReference, IHandlerInfo::GetApplicationIconReference, shell.IHandlerInfo_GetApplicationIconReference, shobjidl_core/IHandlerInfo::GetApplicationIconReference
f1_keywords:
- shobjidl_core/IHandlerInfo.GetApplicationIconReference
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IHandlerInfo.GetApplicationIconReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHandlerInfo::GetApplicationIconReference


## -description


Retrieves the icon of the application that implemented the handler.


## -parameters




### -param value [out]

Type: <b>LPWSTR*</b>

A pointer to a string that, when this method returns successfully, receives the path of the icon.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo">IHandlerInfo</a>
 

 

