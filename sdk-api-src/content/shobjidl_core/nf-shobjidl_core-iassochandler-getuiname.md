---
UID: NF:shobjidl_core.IAssocHandler.GetUIName
title: IAssocHandler::GetUIName
author: windows-sdk-content
description: Retrieves the display name of an application.
old-location: shell\IAssocHandler_GetUIName.htm
old-project: shell
ms.assetid: bf714cf9-a16a-40a4-8dd8-c53c289967f5
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetUIName, GetUIName method [Windows Shell], GetUIName method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],GetUIName method, IAssocHandler.GetUIName, IAssocHandler::GetUIName, _shell_IAssocHandler_GetUIName, shell.IAssocHandler_GetUIName, shobjidl_core/IAssocHandler::GetUIName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IAssocHandler.GetUIName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandler::GetUIName


## -description


Retrieves the display name of an application.


## -parameters




### -param ppsz [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the display name of the application.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/d20aee32-fa5a-40a9-b0e2-8479a90fcf35">IAssocHandler::GetName</a>
 

 

