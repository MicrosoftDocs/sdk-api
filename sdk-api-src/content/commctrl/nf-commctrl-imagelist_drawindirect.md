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

# ImageList_DrawIndirect function


## -description


Draws an image list image based on an <a href="https://msdn.microsoft.com/c3579946-d690-4f32-9662-b4e1b3f06aba">IMAGELISTDRAWPARAMS</a> structure. 


## -parameters




### -param pimldp

Type: <b><a href="https://msdn.microsoft.com/c3579946-d690-4f32-9662-b4e1b3f06aba">IMAGELISTDRAWPARAMS</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c3579946-d690-4f32-9662-b4e1b3f06aba">IMAGELISTDRAWPARAMS</a> structure that contains information about the draw operation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, and zero otherwise. 



