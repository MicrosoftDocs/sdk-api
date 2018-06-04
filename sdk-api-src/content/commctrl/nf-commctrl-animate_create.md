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

# Animate_Create macro


## -description


Creates an animation control. <b>Animate_Create</b> calls the <a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a> function to create the animation control. 


## -parameters




### -param hwndP

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the parent window. 


### -param id

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The child window identifier of the animation control. 


### -param dwStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The window styles. For a list of the animation control style values, see <a href="https://msdn.microsoft.com/ad4fc4fd-166d-4871-9f60-5133a48681aa">Animation Control Styles</a>. 


### -param hInstance

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

A handle to the instance of the module that is creating the animation control. 


## -remarks



The <b>Animate_Create</b> macro sets the width and height of the animation control to zero if the <a href="Animation_Control_Styles.htm">ACS_CENTER</a> style is specified. If the <b>ACS_CENTER</b> style is not specified, <b>Animate_Create</b> sets the width and height based on the dimensions of a frame in the AVI clip. 



