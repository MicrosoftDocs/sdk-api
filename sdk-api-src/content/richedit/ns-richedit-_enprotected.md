---
UID: NS:richedit._enprotected
title: "_enprotected"
author: windows-sdk-content
description: Contains information associated with an EN_PROTECTED notification code. A rich edit control sends this notification when the user attempts to edit protected text.
old-location: controls\ENPROTECTED.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enprotected.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ENPROTECTED, ENPROTECTED structure [Windows Controls], _enprotected, _win32_ENPROTECTED_str, _win32_ENPROTECTED_str_cpp, controls.ENPROTECTED, controls._win32_ENPROTECTED_str, richedit/ENPROTECTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: richedit.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: ENPROTECTED
req.redist: 
---

# _enprotected structure


## -description


Contains information associated with an <a href="https://msdn.microsoft.com/29c0cb51-675c-44b1-ad45-5f7140ca5675">EN_PROTECTED</a> notification code. A rich edit control sends this notification when the user attempts to edit protected text.


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> notification header. 


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

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>

The current selection. 


## -see-also




<a href="https://msdn.microsoft.com/29c0cb51-675c-44b1-ad45-5f7140ca5675">EN_PROTECTED</a>
 

 

