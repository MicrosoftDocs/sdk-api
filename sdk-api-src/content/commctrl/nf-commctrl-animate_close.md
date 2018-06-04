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

# Animate_Close macro


## -description


Closes an AVI clip. You can use this macro or send the <a href="https://msdn.microsoft.com/87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4">ACM_OPEN</a> message explicitly, passing in <b>NULL</b> parameters. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the animation control.


## -remarks



You can use <b>Animate_Close</b> to close an AVI file or AVI resource that was previously opened for the specified animation control.




## -see-also




<a href="https://msdn.microsoft.com/aebfae03-401c-48de-ad3b-14574f5b4e73">Animate_Open</a>
 

 

