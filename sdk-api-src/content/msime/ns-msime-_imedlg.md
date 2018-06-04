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

# _IMEDLG structure


## -description


Used when invoking the Microsoft IME's Dictionary Tool or Word Register Dialog Window from the app.


## -struct-fields




### -field cbIMEDLG

The size of this structure. You must set this value before using the structure.


### -field hwnd

The parent window handle of the Register Word Dialog.


### -field lpwstrWord

<b>NULL</b>, or  the string to be registered. It shows in the Word Register Dialog's "Display" field.


### -field nTabId

The initial tab ID, 0 or 1.


## -see-also




<a href="https://msdn.microsoft.com/E70E3B78-58D7-40E9-8DAB-447B4CBC13F4">IFECommon::InvokeDictToolDialog</a>



<a href="https://msdn.microsoft.com/FBD09E98-9C89-4CE4-9D17-A13E2BE0AB91">IFECommon::InvokeWordRegDialog</a>
 

 

