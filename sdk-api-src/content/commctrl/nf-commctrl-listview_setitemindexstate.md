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

# ListView_SetItemIndexState macro


## -description


Sets the state of a specified list-view item. Use this macro or send the <a href="https://msdn.microsoft.com/9fea6420-320a-4d2a-84b5-7923fbb14655">LVM_SETITEMINDEXSTATE</a> message explicitly.


## -parameters




### -param hwndLV [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control.


### -param plvii [in]

Type: <b><a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/62d28e14-fa0d-42c8-9f8e-afc0cfdff3e3">LVITEMINDEX</a> structure for the item. The caller is responsible for allocating this structure and setting the members.


### -param data [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The state to set on the item as one or more (as a bitwise combination) of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">List-View Item States</a> flags.


### -param mask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The valid bits of the state specified by parameter <i>data</i>. For more information, see the <i>stateMask</i> member of the <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a>) structure.

