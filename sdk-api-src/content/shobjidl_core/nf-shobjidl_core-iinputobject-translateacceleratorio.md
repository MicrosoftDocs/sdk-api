---
UID: NF:shobjidl_core.IInputObject.TranslateAcceleratorIO
title: IInputObject::TranslateAcceleratorIO
author: windows-sdk-content
description: Enables the object to process keyboard accelerators.
old-location: shell\IInputObject_TranslateAcceleratorIO.htm
old-project: shell
ms.assetid: e075556a-2910-41ee-a8f3-3fba1cd55a35
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IInputObject interface [Windows Shell],TranslateAcceleratorIO method, IInputObject.TranslateAcceleratorIO, IInputObject::TranslateAcceleratorIO, TranslateAcceleratorIO, TranslateAcceleratorIO method [Windows Shell], TranslateAcceleratorIO method [Windows Shell],IInputObject interface, _win32_IInputObject_TranslateAcceleratorIO, shell.IInputObject_TranslateAcceleratorIO, shobjidl_core/IInputObject::TranslateAcceleratorIO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Shell32.dll
api_name:
 - IInputObject.TranslateAcceleratorIO
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IInputObject::TranslateAcceleratorIO


## -description


Enables the object to process keyboard accelerators.


## -parameters




### -param pMsg






#### - lpMsg

Type: <b>LPMSG</b>

The address of an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains the keyboard message that is being translated.
        


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if the accelerator was translated, or <b>S_FALSE</b> otherwise.



