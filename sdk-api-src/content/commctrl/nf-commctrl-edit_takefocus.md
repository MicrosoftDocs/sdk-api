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

# Edit_TakeFocus macro


## -description


<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Forces a single-line edit control to receive keyboard focus. You can use this macro or send the <a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a> message explicitly.


## -parameters




### -param hwndCtl

TBD






#### - hwndEdit

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the edit control.


## -remarks



The <a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a> message is ignored if the edit control is not a single-line edit control.

If the edit control previously received an <a href="https://msdn.microsoft.com/aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c">EM_NOSETFOCUS</a> message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.




## -see-also




<a href="https://msdn.microsoft.com/aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c">EM_NOSETFOCUS</a>



<a href="https://msdn.microsoft.com/27470857-4219-4426-bc69-e1271afc6ffb">EM_TAKEFOCUS</a>



<b>Reference</b>
 

 

