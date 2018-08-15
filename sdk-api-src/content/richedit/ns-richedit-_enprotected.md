---
UID: NS:richedit._enprotected
title: "_enprotected"
author: windows-sdk-content
description: Contains information associated with an EN_PROTECTED notification code. A rich edit control sends this notification when the user attempts to edit protected text.
old-location: controls\ENPROTECTED.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enprotected.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ENPROTECTED, ENPROTECTED structure [Windows Controls], _enprotected, _win32_ENPROTECTED_str, _win32_ENPROTECTED_str_cpp, controls.ENPROTECTED, controls._win32_ENPROTECTED_str, richedit/ENPROTECTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ENPROTECTED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - ENPROTECTED
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _enprotected structure


## -description


Contains information associated with an <a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a> notification code. A rich edit control sends this notification when the user attempts to edit protected text.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb775514(v=VS.85).aspx">NMHDR</a> notification header. 


### -field msg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Message that triggered the notification. 


### -field wParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

The <b>wParam</b> parameter of the message. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The <b>lParam</b> parameter of the message. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb787885(v=VS.85).aspx">CHARRANGE</a></b>

The current selection. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787981(v=VS.85).aspx">EN_PROTECTED</a>
 

 

