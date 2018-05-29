---
UID: NF:ole2.OleIsRunning
title: OleIsRunning function
author: windows-sdk-content
description: Determines whether a compound document object is currently in the running state.
old-location: com\oleisrunning.htm
old-project: com
ms.assetid: 9392666f-c269-4667-aeac-67c68bcc5f06
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: OleIsRunning, OleIsRunning function [COM], _ole_OleIsRunning, com.oleisrunning, ole2/OleIsRunning
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: QACONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
api_name:
-	OleIsRunning
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OleIsRunning function


## -description


Determines whether a compound document object is currently in the running state.




## -parameters




### -param pObject [in]

Pointer to the <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface on the object of interest.


## -returns



The return value is <b>TRUE</b> if the object is running; otherwise, it is <b>FALSE</b>.





## -remarks



You can use <b>OleIsRunning</b> and <a href="https://msdn.microsoft.com/0a4cdd21-8256-4533-9cad-d9e8450a17e9">IRunnableObject::IsRunning</a> interchangeably. <b>OleIsRunning</b> queries the object for a pointer to the <a href="https://msdn.microsoft.com/c682447b-5b12-41d5-a81d-fe94a117f740">IRunnableObject</a> interface and calls its <b>IRunnableObject::IsRunning</b> method. If successful, the function returns the results of the call to <b>IRunnableObject::IsRunning</b>.






## -see-also




<a href="https://msdn.microsoft.com/0a4cdd21-8256-4533-9cad-d9e8450a17e9">IRunnableObject::IsRunning</a>
 

 

