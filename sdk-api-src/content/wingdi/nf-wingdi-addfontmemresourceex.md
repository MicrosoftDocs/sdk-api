---
UID: NF:wingdi.AddFontMemResourceEx
title: AddFontMemResourceEx function (wingdi.h)
description: The AddFontMemResourceEx function adds the font resource from a memory image to the system.
helpviewer_keywords: ["AddFontMemResourceEx","AddFontMemResourceEx function [Windows GDI]","_win32_AddFontMemResourceEx","gdi.addfontmemresourceex","wingdi/AddFontMemResourceEx"]
old-location: gdi\addfontmemresourceex.htm
tech.root: gdi
ms.assetid: ad5153ba-fa9d-4a07-9be3-a07b524c1539
ms.date: 12/05/2018
ms.keywords: AddFontMemResourceEx, AddFontMemResourceEx function [Windows GDI], _win32_AddFontMemResourceEx, gdi.addfontmemresourceex, wingdi/AddFontMemResourceEx
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddFontMemResourceEx
 - wingdi/AddFontMemResourceEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - AddFontMemResourceEx
---

# AddFontMemResourceEx function


## -description

The <b>AddFontMemResourceEx</b> function adds the font resource from a memory image to the system.

## -parameters

### -param pFileView [in]

A pointer to a font resource.

### -param cjSize [in]

The number of bytes in the font resource that is pointed to by <i>pbFont</i>.

### -param pvResrved [in]

Reserved. Must be 0.

### -param pNumFonts [in]

A pointer to a variable that specifies the number of fonts installed.

## -returns

If the function succeeds, the return value specifies the handle to the font added. This handle uniquely identifies the fonts that were installed on the system. If the function fails, the return value is zero. No extended error information is available.

## -remarks

This function allows an application to get a font that is embedded in a document or a webpage. A font that is added by <b>AddFontMemResourceEx</b> is always private to the process that made the call and is not enumerable.

A memory image can contain more than one font. When this function succeeds, <i>pcFonts</i> is a pointer to a <b>DWORD</b> whose value is the number of fonts added to the system as a result of this call. For example, this number could be 2 for the vertical and horizontal faces of an Asian font.

When the function succeeds, the caller of this function can free the memory pointed to by <i>pbFont</i> because the system has made its own copy of the memory. To remove the fonts that were installed, call <a href="/windows/desktop/api/wingdi/nf-wingdi-removefontmemresourceex">RemoveFontMemResourceEx</a>. However, when the process goes away, the system will unload the fonts even if the process did not call <a href="/windows/desktop/api/wingdi/nf-wingdi-removefontmemresourceex">RemoveFontMemResource</a>.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-designvector">DESIGNVECTOR
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-removefontmemresourceex">RemoveFontMemResourceEx
      </a>



<a href="/previous-versions/windows/desktop/oe/oe-ihttpmailtransport-sendmessage">SendMessage</a>