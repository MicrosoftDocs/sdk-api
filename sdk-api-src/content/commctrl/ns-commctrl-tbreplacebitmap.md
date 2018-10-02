---
UID: NS:commctrl.TBREPLACEBITMAP
title: TBREPLACEBITMAP
author: windows-sdk-content
description: Used with the TB_REPLACEBITMAP message to replace one toolbar bitmap with another.
old-location: controls\TBREPLACEBITMAP.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\tbreplacebitmap.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPTBREPLACEBITMAP, LPTBREPLACEBITMAP, LPTBREPLACEBITMAP structure pointer [Windows Controls], TBREPLACEBITMAP, TBREPLACEBITMAP structure [Windows Controls], _win32_TBREPLACEBITMAP, _win32_TBREPLACEBITMAP_cpp, commctrl/LPTBREPLACEBITMAP, commctrl/TBREPLACEBITMAP, controls.TBREPLACEBITMAP, controls._win32_TBREPLACEBITMAP"
ms.prod: windows
ms.technology: windows-sdk
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
 - TBREPLACEBITMAP
product: Windows
targetos: Windows
req.typenames: TBREPLACEBITMAP, *LPTBREPLACEBITMAP
req.redist: 
---

# TBREPLACEBITMAP structure


## -description


Used with the <a href="https://msdn.microsoft.com/abad5c7a-ebdd-46b5-a465-fe64ff8eb127">TB_REPLACEBITMAP</a> message to replace one toolbar bitmap with another.


## -struct-fields




### -field hInstOld

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Module instance handle to the bitmap resource being replaced. Set this member to <b>NULL</b> to instead use a bitmap handle. 


### -field nIDOld

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

If 
					<b>hInstOld</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap that is being replaced. Otherwise, set it to the resource identifier of the bitmap being replaced. 


### -field hInstNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HINSTANCE</a></b>

Module instance handle that contains the new bitmap resource. Set this member to <b>NULL</b> to instead use a bitmap handle. 


### -field nIDNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT_PTR</a></b>

If 
					<b>hInstNew</b> is <b>NULL</b>, set this member to the bitmap handle of the bitmap with the new button images. Otherwise, set it to the resource identifier of the bitmap with the new button images. 


### -field nButtons

Type: <b>int</b>

Number of button images contained in the new bitmap. The number of new images should be the same as the number of replaced images.


## -remarks



If 
				<b>nIDNew</b> holds a bitmap handle, rather than a resource ID, do not destroy the bitmap until it has been replaced with <a href="https://msdn.microsoft.com/abad5c7a-ebdd-46b5-a465-fe64ff8eb127">TB_REPLACEBITMAP</a>, or the toolbar is destroyed.



