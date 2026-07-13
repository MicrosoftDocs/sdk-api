---
UID: NF:ole2.OleIsRunning
title: OleIsRunning function (ole2.h)
description: Determines whether a compound document object is currently in the running state.
helpviewer_keywords: ["OleIsRunning","OleIsRunning function [COM]","_ole_OleIsRunning","com.oleisrunning","ole2/OleIsRunning"]
old-location: com\oleisrunning.htm
tech.root: com
ms.assetid: 9392666f-c269-4667-aeac-67c68bcc5f06
ms.date: 12/05/2018
ms.keywords: OleIsRunning, OleIsRunning function [COM], _ole_OleIsRunning, com.oleisrunning, ole2/OleIsRunning
req.header: ole2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleIsRunning
 - ole2/OleIsRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - ext-ms-win-com-ole32-l1-1-4.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - ext-ms-win-com-ole32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-1.dll
 - ext-ms-win-com-ole32-l1-1-0.dll
 - Ole32.dll
api_name:
 - OleIsRunning
---

# OleIsRunning function


## -description

Determines whether a compound document object is currently in the running state.

## -parameters

### -param pObject [in]

Pointer to the <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface on the object of interest.

## -returns

The return value is <b>TRUE</b> if the object is running; otherwise, it is <b>FALSE</b>.

## -remarks

You can use <b>OleIsRunning</b> and <a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-isrunning">IRunnableObject::IsRunning</a> interchangeably. <b>OleIsRunning</b> queries the object for a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> interface and calls its <b>IRunnableObject::IsRunning</b> method. If successful, the function returns the results of the call to <b>IRunnableObject::IsRunning</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-irunnableobject-isrunning">IRunnableObject::IsRunning</a>