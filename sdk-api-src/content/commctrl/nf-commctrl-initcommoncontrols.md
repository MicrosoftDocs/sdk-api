---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# InitCommonControls function


## -description


Registers and initializes certain common control window classes. This function is obsolete. New applications should use the <a href="https://msdn.microsoft.com/a0ca2152-673e-4920-ae78-1421fdec1a05">InitCommonControlsEx</a> function. 


## -parameters






## -returns



This function does not return a value.




## -remarks



Under Comctl32.dll version 5.x, only Windows 95 classes (ICC_WIN95_CLASSES) can be registered through <b>InitCommonControls</b>. Programs which require additional common control classes must use the <a href="https://msdn.microsoft.com/a0ca2152-673e-4920-ae78-1421fdec1a05">InitCommonControlsEx</a> function.

Under Comctl32.dll version 6.0 and later, <b>InitCommonControls</b> does nothing. Applications must explicitly register all common controls through <a href="https://msdn.microsoft.com/a0ca2152-673e-4920-ae78-1421fdec1a05">InitCommonControlsEx</a>.



