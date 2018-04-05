---
UID: NF:uiautomationcoreapi.UiaSetFocus
title: UiaSetFocus function
author: windows-driver-content
description: Sets the input focus to the specified element in the UI.
old-location: winauto\uiauto_UiaSetFocusAutoMeth.htm
old-project: WinAuto
ms.assetid: 89cc1c0d-b6c2-434d-b849-cf09b1711a3d
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: UiaSetFocus, UiaSetFocus function [Windows Accessibility], uiauto.uiauto_UiaSetFocusAutoMeth, uiauto_UiaSetFocusAutoMeth, uiautomationcoreapi/UiaSetFocus, winauto.uiauto_UiaSetFocusAutoMeth
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
api_name:
-	UiaSetFocus
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaSetFocus function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Sets the input focus to the specified element in the UI.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The element that receives focus.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



