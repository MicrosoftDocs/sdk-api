---
UID: NF:commctrl.Edit_ShowBalloonTip
title: Edit_ShowBalloonTip macro
author: windows-sdk-content
description: Displays a balloon tip associated with an edit control. You can use this macro or send the EM_SHOWBALLOONTIP message explicitly.
old-location: controls\Edit_ShowBalloonTip.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_showballoontip.htm
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Edit_ShowBalloonTip, Edit_ShowBalloonTip macro [Windows Controls], _win32_Edit_ShowBalloonTip, _win32_Edit_ShowBalloonTip_cpp, commctrl/Edit_ShowBalloonTip, controls.Edit_ShowBalloonTip, controls._win32_Edit_ShowBalloonTip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	Edit_ShowBalloonTip
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

