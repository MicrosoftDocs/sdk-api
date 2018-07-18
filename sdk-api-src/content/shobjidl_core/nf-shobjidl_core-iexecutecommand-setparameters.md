---
UID: NF:shobjidl_core.IExecuteCommand.SetParameters
title: IExecuteCommand::SetParameters
author: windows-sdk-content
description: Provides parameter values for the verb.
old-location: shell\IExecuteCommand_SetParameters.htm
old-project: shell
ms.assetid: 3e08777c-865b-49c2-8f37-1a427c4945b4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IExecuteCommand interface [Windows Shell],SetParameters method, IExecuteCommand.SetParameters, IExecuteCommand::SetParameters, SetParameters, SetParameters method [Windows Shell], SetParameters method [Windows Shell],IExecuteCommand interface, _shell_IExecuteCommand_SetParameters, shell.IExecuteCommand_SetParameters, shobjidl_core/IExecuteCommand::SetParameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IExecuteCommand.SetParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IExecuteCommand::SetParameters


## -description


Provides parameter values for the verb.


## -parameters




### -param pszParameters [in]

Type: <b>LPCWSTR</b>

Pointer to a string that contains parameter values. The format and contents of this string is determined by the verb that is to be invoked.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



