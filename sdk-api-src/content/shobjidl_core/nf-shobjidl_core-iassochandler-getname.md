---
UID: NF:shobjidl_core.IAssocHandler.GetName
title: IAssocHandler::GetName
author: windows-sdk-content
description: Retrieves the full path and file name of the executable file associated with the file type.
old-location: shell\IAssocHandler_GetName.htm
old-project: shell
ms.assetid: d20aee32-fa5a-40a9-b0e2-8479a90fcf35
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],IAssocHandler interface, IAssocHandler interface [Windows Shell],GetName method, IAssocHandler.GetName, IAssocHandler::GetName, _shell_IAssocHandler_GetName, shell.IAssocHandler_GetName, shobjidl_core/IAssocHandler::GetName
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IAssocHandler.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IAssocHandler::GetName


## -description


Retrieves the full path and file name of the executable file associated with the file type.


## -parameters




### -param ppsz [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated, Unicode string that contains the full path of the file, including the file name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a>



<a href="https://msdn.microsoft.com/bf714cf9-a16a-40a4-8dd8-c53c289967f5">IAssocHandler::GetUIName</a>
 

 

