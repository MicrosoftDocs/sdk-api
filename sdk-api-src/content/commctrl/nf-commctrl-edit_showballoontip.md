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

# Edit_ShowBalloonTip macro


## -description


Displays a balloon tip associated with an edit control. You can use this macro or send the <a href="https://msdn.microsoft.com/1e6915b7-4b61-43b2-be13-b89c72378a1a">EM_SHOWBALLOONTIP</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control. 


### -param peditballoontip

Type: <b>PEDITBALLOONTIP</b>

A pointer to an <a href="https://msdn.microsoft.com/d8325283-d059-4494-9b99-e473459bbdcc">EDITBALLOONTIP</a> structure that contains information about the balloon tip to display. 


## -remarks



<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comclt32.dll version 6.0. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d8325283-d059-4494-9b99-e473459bbdcc">EDITBALLOONTIP</a>



<a href="https://msdn.microsoft.com/1e6915b7-4b61-43b2-be13-b89c72378a1a">EM_SHOWBALLOONTIP</a>



<a href="https://msdn.microsoft.com/2a71b92c-f57a-4c27-80b7-e1d9092f3701">Edit Controls</a>



<b>Reference</b>
 

 

