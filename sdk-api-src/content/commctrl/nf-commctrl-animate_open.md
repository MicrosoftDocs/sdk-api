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

# Animate_Open macro


## -description


Opens an AVI clip and displays its first frame in an animation control. You can use this macro or send the <a href="https://msdn.microsoft.com/87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4">ACM_OPEN</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param szName

TBD






#### - hwndAnim

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the animation control. 


#### - lpszName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource. Alternatively, this parameter can consist of the AVI resource identifier in the <a href="https://msdn.microsoft.com/4f169f33-ed13-4efc-bf3f-ea2a4fe1de4e">LOWORD</a> and zero in the <a href="https://msdn.microsoft.com/9f79d489-ff3f-437c-821e-fd353d712c7b">HIWORD</a>. To create this value, use the <a href="https://msdn.microsoft.com/761df981-776f-43ca-9cc9-bb82a49f66e6">MAKEINTRESOURCE</a> macro. The control loads an AVI resource from the module specified by the instance handle passed to the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> function, the <a href="https://msdn.microsoft.com/d62e0341-8d12-4e66-80da-3a797a12d0a3">Animate_Create</a> macro, or the dialog box creation function that created the control. The AVI file or resource specified by <i>lpszName</i> must not contain audio.



If this parameter is <b>NULL</b>, the system closes the AVI file that was previously opened for the specified animation control, if any.


## -remarks



You can only open silent AVI clips. <a href="https://msdn.microsoft.com/87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4">ACM_OPEN</a> and <b>Animate_Open</b> will fail if <i>lpszName</i> specifies an AVI clip that contains sound. 

You can use <a href="https://msdn.microsoft.com/e5997bda-2eb0-452b-a9c3-11ca7110d0fb">Animate_Close</a> to close an AVI file or AVI resource that was previously opened for the specified animation control. 



