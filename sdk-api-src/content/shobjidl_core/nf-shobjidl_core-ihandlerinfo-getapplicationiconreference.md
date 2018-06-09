---
UID: NF:shobjidl_core.IHandlerInfo.GetApplicationIconReference
title: IHandlerInfo::GetApplicationIconReference
author: windows-sdk-content
description: Retrieves the icon of the application that implemented the handler.
old-location: shell\IHandlerInfo_GetApplicationIconReference.htm
old-project: shell
ms.assetid: be886508-16a5-4a77-9fa4-b6a8d028c9e9
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetApplicationIconReference, GetApplicationIconReference method [Windows Shell], GetApplicationIconReference method [Windows Shell],IHandlerInfo interface, IHandlerInfo interface [Windows Shell],GetApplicationIconReference method, IHandlerInfo.GetApplicationIconReference, IHandlerInfo::GetApplicationIconReference, shell.IHandlerInfo_GetApplicationIconReference, shobjidl_core/IHandlerInfo::GetApplicationIconReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IHandlerInfo.GetApplicationIconReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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




<a href="https://msdn.microsoft.com/f0b8da9f-75ee-418d-8df6-fa0d7c600e62">IHandlerInfo</a>
 

 

