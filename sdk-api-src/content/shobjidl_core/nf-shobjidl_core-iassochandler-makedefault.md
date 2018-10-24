---
UID: NF:shobjidl_core.IAssocHandler.MakeDefault
title: IAssocHandler::MakeDefault
author: windows-sdk-content
description: Sets an application as the default application for this file type.
old-location: shell\IAssocHandler_MakeDefault.htm
tech.root: shell
ms.assetid: 106ac493-bde6-4327-b3be-3132bfd47415
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IAssocHandler interface [Windows Shell],MakeDefault method, IAssocHandler.MakeDefault, IAssocHandler::MakeDefault, MakeDefault, MakeDefault method [Windows Shell], MakeDefault method [Windows Shell],IAssocHandler interface, _shell_IAssocHandler_MakeDefault, shell.IAssocHandler_MakeDefault, shobjidl_core/IAssocHandler::MakeDefault
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAssocHandler.MakeDefault
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAssocHandler::MakeDefault


## -description


Sets an application as the default application for this file type.


## -parameters




### -param pszDescription [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated, Unicode string that contains the display name of the application.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/bf714cf9-a16a-40a4-8dd8-c53c289967f5">IAssocHandler::GetUIName</a>
 

 

