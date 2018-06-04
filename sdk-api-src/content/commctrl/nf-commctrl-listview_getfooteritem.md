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

# ListView_GetFooterItem macro


## -description


Gets information on a footer item for a specified list-view control. Use this macro or send the <a href="https://msdn.microsoft.com/92f55719-c265-433f-84fc-a673680c7ad9">LVM_GETFOOTERITEM</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param iItem [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An index of the item.


### -param pfi [in, out]

Type: <b><a href="https://msdn.microsoft.com/b993616d-1eb2-4c9b-ac05-de1abd3e1ff7">LVFOOTERITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/b993616d-1eb2-4c9b-ac05-de1abd3e1ff7">LVFOOTERITEM</a> structure to receive a value for the <i>state</i> and/or <i>pszText</i> members according to the value of the <i>mask</i> member. The caller is responsible for allocating this structure and setting its members to indicate to the receiver what information to return. For more information, see <b>LVFOOTERITEM</b>.

