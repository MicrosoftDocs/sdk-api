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

# ListView_GetFooterInfo macro


## -description


Gets information on the footer of a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/5734e151-50c0-46df-8f2c-220c4910a590">LVM_GETFOOTERINFO</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param plvfi [in, out]

Type: <b>LPLVFOOTERINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/e988eb29-3ea1-4af5-b908-45832a7acadd">LVFOOTERINFO</a> structure to receive information depending on the value of the <b>mask</b> member. The calling application is responsible for allocating this structure and setting the <b>mask</b> member.

