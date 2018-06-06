---
UID: NF:shobjidl_core.IIOCancelInformation.GetCancelInformation
title: IIOCancelInformation::GetCancelInformation
author: windows-sdk-content
description: Returns information that is posted when a user selects Cancel from the progress UI.
old-location: shell\IIOCancelInformation_GetCancelInformation.htm
old-project: shell
ms.assetid: 201537b5-1866-4df6-a51d-3f07c18fe0c8
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetCancelInformation, GetCancelInformation method [Windows Shell], GetCancelInformation method [Windows Shell],IIOCancelInformation interface, IIOCancelInformation interface [Windows Shell],GetCancelInformation method, IIOCancelInformation.GetCancelInformation, IIOCancelInformation::GetCancelInformation, _shell_IIOCancelInformation_GetCancelInformation, shell.IIOCancelInformation_GetCancelInformation, shobjidl_core/IIOCancelInformation::GetCancelInformation
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
req.idl: 
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
 - Shell32.dll
api_name:
 - IIOCancelInformation.GetCancelInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IIOCancelInformation::GetCancelInformation


## -description


Returns information that is posted when a user selects <b>Cancel</b> from the progress UI. The process thread uses this method to find out which message the progress dialog will send to the process thread when the user hits cancel.  The process thread then listens for this message and does its own cleanup upon receipt.



## -parameters




### -param pdwThreadID [out]

Type: <b>DWORD*</b>

When this method returns, contains a pointer to the ID of the process thread.


### -param puMsgCancel [out]

Type: <b>UINT*</b>

When this method returns, contains a pointer to <i>uMsgCancel</i> that the process thread should post if the operation is canceled.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



