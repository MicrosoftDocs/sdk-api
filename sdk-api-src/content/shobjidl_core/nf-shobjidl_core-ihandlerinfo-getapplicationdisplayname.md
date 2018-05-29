---
UID: NF:shobjidl_core.IHandlerInfo.GetApplicationDisplayName
title: IHandlerInfo::GetApplicationDisplayName
author: windows-sdk-content
description: Retrieves the display name of the application that implemented the handler.
old-location: shell\IHandlerInfo_GetApplicationDisplayName.htm
old-project: shell
ms.assetid: 19b3b042-7c2d-4402-913e-daa5c8bba595
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetApplicationDisplayName, GetApplicationDisplayName method [Windows Shell], GetApplicationDisplayName method [Windows Shell],IHandlerInfo interface, IHandlerInfo interface [Windows Shell],GetApplicationDisplayName method, IHandlerInfo.GetApplicationDisplayName, IHandlerInfo::GetApplicationDisplayName, shell.IHandlerInfo_GetApplicationDisplayName, shobjidl_core/IHandlerInfo::GetApplicationDisplayName
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IHandlerInfo.GetApplicationDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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




<a href="https://msdn.microsoft.com/f0b8da9f-75ee-418d-8df6-fa0d7c600e62">IHandlerInfo</a>
 

 

