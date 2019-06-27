---
UID: NF:ole2.OleIsRunning
title: OleIsRunning function (ole2.h)
author: windows-sdk-content
description: Determines whether a compound document object is currently in the running state.
old-location: com\oleisrunning.htm
tech.root: com
ms.assetid: 9392666f-c269-4667-aeac-67c68bcc5f06
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OleIsRunning, OleIsRunning function [COM], _ole_OleIsRunning, com.oleisrunning, ole2/OleIsRunning
ms.topic: function
f1_keywords: 
 - "ole2/OleIsRunning"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - OleIsRunning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleIsRunning function


## -description


Determines whether a compound document object is currently in the running state.




## -parameters




### -param pObject [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface on the object of interest.


## -returns



The return value is <b>TRUE</b> if the object is running; otherwise, it is <b>FALSE</b>.





## -remarks



You can use <b>OleIsRunning</b> and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-isrunning">IRunnableObject::IsRunning</a> interchangeably. <b>OleIsRunning</b> queries the object for a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-irunnableobject">IRunnableObject</a> interface and calls its <b>IRunnableObject::IsRunning</b> method. If successful, the function returns the results of the call to <b>IRunnableObject::IsRunning</b>.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-irunnableobject-isrunning">IRunnableObject::IsRunning</a>
 

 

