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

# ComboBox_GetCueBannerText macro


## -description


Gets the cue banner text displayed in the edit control of a combo box. Use this macro or send the <a href="https://msdn.microsoft.com/38959228-9f07-4636-a1ea-681efe77b9ec">CB_GETCUEBANNER</a> message explicitly.


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the combo box.


### -param lpwText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPWSTR</a></b>

A pointer to a Unicode string buffer that receives the cue banner text. The calling application is responsible for allocating the memory for the buffer. The buffer size must be equal to the length of the cue banner string in <b>WCHAR</b><b>s</b>, plus 1—for the terminating <b>NULL</b> <b>WCHAR</b>.


### -param cchText

Type: <b>int</b>

The size of the buffer pointed to by <i>lpwText</i> in <b>WCHAR</b><b>s</b>. 
               


## -see-also




<a href="https://msdn.microsoft.com/7102beff-7f67-4e4e-a32b-9ccae1522ebd">Combo Box Features</a>
 

 

