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

# Button_GetNoteLength macro


## -description


Gets the length of the note text that may be displayed in the description for a command link. Use this macro or send the <a href="https://msdn.microsoft.com/62385485-b553-47e9-9f15-696cc4694752">BCM_GETNOTELENGTH</a> message explicitly.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the button control.


## -remarks



Beginning with comctl32 DLL version 6.01, command link buttons may have a note. For information on DLL versions, see <a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Common Control Versions</a>.

The <b>Button_GetNoteLength</b> macro works only with the <a href="Button_Styles.htm">BS_COMMANDLINK</a> and <a href="Button_Styles.htm">BS_DEFCOMMANDLINK</a> button styles.




## -see-also




<a href="https://msdn.microsoft.com/30254cb5-43cd-407f-8ad6-bd7f9ec3edc7">Button Styles</a>



<a href="https://msdn.microsoft.com/bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b">Button Types</a>



<b>Conceptual</b>



<b>Reference</b>
 

 

