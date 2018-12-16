---
UID: NS:commctrl.tagCOLORSCHEME
title: COLORSCHEME
author: windows-sdk-content
description: Contains information for the drawing of buttons in a toolbar or rebar.
old-location: controls\COLORSCHEME.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\structures\colorscheme.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPCOLORSCHEME, COLORSCHEME, COLORSCHEME structure [Windows Controls], LPCOLORSCHEME, LPCOLORSCHEME structure pointer [Windows Controls], _win32_COLORSCHEME, _win32_COLORSCHEME_cpp, commctrl/COLORSCHEME, commctrl/LPCOLORSCHEME, controls.COLORSCHEME, controls._win32_COLORSCHEME"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - COLORSCHEME
product: Windows
targetos: Windows
req.typenames: COLORSCHEME, *LPCOLORSCHEME
req.redist: 
---

# COLORSCHEME structure


## -description


Contains information for the drawing of buttons in a toolbar or rebar. 


## -struct-fields




### -field dwSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The size of this structure, in bytes. 


### -field clrBtnHighlight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that represents the highlight color of the buttons. Use 
					<b>CLR_DEFAULT</b> for the default highlight color. 


### -field clrBtnShadow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value that represents the shadow color of the buttons. Use 
					<b>CLR_DEFAULT</b> for the default shadow color. 

