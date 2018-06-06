---
UID: NS:richedit._enlink
title: "_enlink"
author: windows-sdk-content
description: Contains information about an EN_LINK notification code from a rich edit control.
old-location: controls\ENLINK.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\enlink.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ENLINK, ENLINK structure [Windows Controls], _enlink, _win32_ENLINK_str, _win32_ENLINK_str_cpp, controls.ENLINK, controls._win32_ENLINK_str, richedit/ENLINK
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
tech.root: 
req.typenames: ENLINK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - ENLINK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _enlink structure


## -description



	 Contains information about an <a href="https://msdn.microsoft.com/67f02908-957e-4d91-8a70-70399ce9cf2e">EN_LINK</a> notification code from a rich edit control. 


## -struct-fields




### -field nmhdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


			 The code member of this structure identifies the notification code being sent. 


### -field msg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Identifier of the message that caused the rich edit control to send the <a href="https://msdn.microsoft.com/67f02908-957e-4d91-8a70-70399ce9cf2e">EN_LINK</a> notification code. 


### -field wParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

The <b>wParam</b> parameter of the message received by the rich edit control. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The <b>lParam</b> parameter of the message received by the rich edit control. 


### -field chrg

Type: <b><a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a></b>


			 The range of consecutive characters in the rich edit control that have the CFE_LINK effect. 


## -see-also




<a href="https://msdn.microsoft.com/144aadcb-92c9-408b-b2ae-a0a4e12c4759">CHARRANGE</a>



<a href="https://msdn.microsoft.com/67f02908-957e-4d91-8a70-70399ce9cf2e">EN_LINK</a>



<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a>



<b>Reference</b>
 

 

