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

# MonthCal_HitTest macro


## -description


Determines which portion of a month calendar control is at a given point on the screen. You can use this macro or send the <a href="https://msdn.microsoft.com/51e74b07-4ed7-488d-ad5d-116f046577fc">MCM_HITTEST</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param pinfo

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - pMCHitTest

Type: <b>PMCHITTESTINFO</b>

Pointer to an <a href="https://msdn.microsoft.com/82597f85-25c9-416a-b9b9-fee84f7480d7">MCHITTESTINFO</a> structure. Upon calling the macro, the <b>cbSize</b> member must be set to the size of the <b>MCHITTESTINFO</b> structure, and <b>pt</b> must be set to the point you want to hit test. 

