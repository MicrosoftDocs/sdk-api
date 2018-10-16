---
UID: NF:prsht.PropSheet_QuerySiblings
title: PropSheet_QuerySiblings macro
author: windows-sdk-content
description: Causes a property sheet to send the PSM_QUERYSIBLINGS message to each of its pages. You can use this macro or send the PSM_QUERYSIBLINGS message explicitly.
old-location: controls\PropSheet_QuerySiblings.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\propsheet\macros\propsheet_querysiblings.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: PropSheet_QuerySiblings, PropSheet_QuerySiblings macro [Windows Controls], _win32_PropSheet_QuerySiblings, _win32_PropSheet_QuerySiblings_cpp, controls.PropSheet_QuerySiblings, controls._win32_PropSheet_QuerySiblings, prsht/PropSheet_QuerySiblings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: prsht.h
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
 - Prsht.h
api_name:
 - PropSheet_QuerySiblings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PropSheet_QuerySiblings macro


## -description


Causes a property sheet to send the <a href="https://msdn.microsoft.com/96f48847-b7b8-4d6f-8bde-ada915b7c962">PSM_QUERYSIBLINGS</a> message to each of its pages. You can use this macro or send the <b>PSM_QUERYSIBLINGS</b> message explicitly.


## -parameters




### -param hDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet.


### -param wParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">WPARAM</a></b>

First application-defined parameter.


### -param lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Second application-defined parameter.


## -remarks



If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.



