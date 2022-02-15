---
UID: NF:shobjidl_core.IIOCancelInformation.GetCancelInformation
title: IIOCancelInformation::GetCancelInformation (shobjidl_core.h)
description: Returns information that is posted when a user selects Cancel from the progress UI.
helpviewer_keywords: ["GetCancelInformation","GetCancelInformation method [Windows Shell]","GetCancelInformation method [Windows Shell]","IIOCancelInformation interface","IIOCancelInformation interface [Windows Shell]","GetCancelInformation method","IIOCancelInformation.GetCancelInformation","IIOCancelInformation::GetCancelInformation","_shell_IIOCancelInformation_GetCancelInformation","shell.IIOCancelInformation_GetCancelInformation","shobjidl_core/IIOCancelInformation::GetCancelInformation"]
old-location: shell\IIOCancelInformation_GetCancelInformation.htm
tech.root: shell
ms.assetid: 201537b5-1866-4df6-a51d-3f07c18fe0c8
ms.date: 12/05/2018
ms.keywords: GetCancelInformation, GetCancelInformation method [Windows Shell], GetCancelInformation method [Windows Shell],IIOCancelInformation interface, IIOCancelInformation interface [Windows Shell],GetCancelInformation method, IIOCancelInformation.GetCancelInformation, IIOCancelInformation::GetCancelInformation, _shell_IIOCancelInformation_GetCancelInformation, shell.IIOCancelInformation_GetCancelInformation, shobjidl_core/IIOCancelInformation::GetCancelInformation
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
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IIOCancelInformation::GetCancelInformation
 - shobjidl_core/IIOCancelInformation::GetCancelInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IIOCancelInformation.GetCancelInformation
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

