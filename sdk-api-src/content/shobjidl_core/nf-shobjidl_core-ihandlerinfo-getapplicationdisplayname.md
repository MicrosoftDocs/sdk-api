---
UID: NF:shobjidl_core.IHandlerInfo.GetApplicationDisplayName
title: IHandlerInfo::GetApplicationDisplayName (shobjidl_core.h)
description: Retrieves the display name of the application that implemented the handler.
helpviewer_keywords: ["GetApplicationDisplayName","GetApplicationDisplayName method [Windows Shell]","GetApplicationDisplayName method [Windows Shell]","IHandlerInfo interface","IHandlerInfo interface [Windows Shell]","GetApplicationDisplayName method","IHandlerInfo.GetApplicationDisplayName","IHandlerInfo::GetApplicationDisplayName","shell.IHandlerInfo_GetApplicationDisplayName","shobjidl_core/IHandlerInfo::GetApplicationDisplayName"]
old-location: shell\IHandlerInfo_GetApplicationDisplayName.htm
tech.root: shell
ms.assetid: 19b3b042-7c2d-4402-913e-daa5c8bba595
ms.date: 12/05/2018
ms.keywords: GetApplicationDisplayName, GetApplicationDisplayName method [Windows Shell], GetApplicationDisplayName method [Windows Shell],IHandlerInfo interface, IHandlerInfo interface [Windows Shell],GetApplicationDisplayName method, IHandlerInfo.GetApplicationDisplayName, IHandlerInfo::GetApplicationDisplayName, shell.IHandlerInfo_GetApplicationDisplayName, shobjidl_core/IHandlerInfo::GetApplicationDisplayName
f1_keywords:
- shobjidl_core/IHandlerInfo.GetApplicationDisplayName
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
- IHandlerInfo.GetApplicationDisplayName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHandlerInfo::GetApplicationDisplayName


## -description


Retrieves the display name of the application that implemented the handler.


## -parameters




### -param value [out]

Type: <b>LPWSTR*</b>

A pointer to a string that, when this method returns successfully, receives the display name. If no display name could be found, the name of the application's .exe file is used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo">IHandlerInfo</a>
 

 

