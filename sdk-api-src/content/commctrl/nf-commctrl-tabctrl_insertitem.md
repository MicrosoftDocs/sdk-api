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

# TabCtrl_InsertItem macro


## -description


Inserts a new tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/e547c49a-699c-4137-8680-20391d138d54">TCM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param iItem

Type: <b>int</b>

Index of the new tab. 


### -param pitem

Type: <b>const LPTCITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure that specifies the attributes of the tab. The <b>dwState</b> and <b>dwStateMask</b> members of this structure are ignored by this message. 

