---
UID: NF:ctfutb.ITfMenu.AddMenuItem
title: ITfMenu::AddMenuItem (ctfutb.h)
description: ITfMenu::AddMenuItem method
helpviewer_keywords: ["AddMenuItem","AddMenuItem method [Text Services Framework]","AddMenuItem method [Text Services Framework]","ITfMenu interface","ITfMenu interface [Text Services Framework]","AddMenuItem method","ITfMenu.AddMenuItem","ITfMenu::AddMenuItem","_tsf_itfmenu_addmenuitem_ref","ctfutb/ITfMenu::AddMenuItem","tsf.itfmenu_addmenuitem"]
old-location: tsf\itfmenu_addmenuitem.htm
tech.root: TSF
ms.assetid: c00048d1-d7c1-4ea3-a132-5f5aa570148f
ms.date: 12/05/2018
ms.keywords: AddMenuItem, AddMenuItem method [Text Services Framework], AddMenuItem method [Text Services Framework],ITfMenu interface, ITfMenu interface [Text Services Framework],AddMenuItem method, ITfMenu.AddMenuItem, ITfMenu::AddMenuItem, _tsf_itfmenu_addmenuitem_ref, ctfutb/ITfMenu::AddMenuItem, tsf.itfmenu_addmenuitem
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfMenu::AddMenuItem
 - ctfutb/ITfMenu::AddMenuItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfMenu.AddMenuItem
---

# ITfMenu::AddMenuItem


## -description

Adds an item to the menu that the language bar will display for the button.

## -parameters

### -param uId [in]

Contains the menu item identifier.

### -param dwFlags [in]

Contains zero or a combination of one or more of the <a href="/windows/desktop/TSF/tf-lbmenuf--constants">TF_LBMENUF_*</a> values that specify the type and state of the menu item.

### -param hbmp [in]

Contains the handle of the bitmap drawn for the menu item. If this is <b>NULL</b>, no bitmap is displayed for the menu item.

### -param hbmpMask [in]

Contains the handle of the mask bitmap. This is a monochrome bitmap that functions as a mask for <i>hbmp</i>. Each black pixel in this bitmap will cause the corresponding pixel in <i>hbmp</i> to be displayed in its normal color. Each white pixel in this bitmap will cause the corresponding pixel in <i>hbmp</i> to be displayed in the inverse of its normal color.

To have the bitmap displayed without any color conversion, create a monochrome bitmap the same size as <i>hbmp</i> and set each pixel to black (RGB(0, 0, 0)).

If <i>hbmp</i> is <b>NULL</b>, this parameter is ignored.

### -param pch [in]

Pointer to a <b>WCHAR</b> buffer that contains the text to be displayed for the menu item. The length of the text is specified by <i>cch</i>.

### -param cch [in]

Specifies the length, in <b>WCHAR</b>, of the menu item text in <i>pch</i>.

### -param ppMenu

[in, out] Pointer to an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu</a> interface pointer that receives the submenu object. This parameter is not used and must be <b>NULL</b> if <i>dwFlags</i> does not contain <b>TF_LBMENUF_SUBMENU</b>.

If the submenu item is successfully created, this parameter receives an <a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu</a> object that the caller uses to add items to the submenu.

If <i>dwFlags</i> contains <b>TF_LBMENUF_SUBMENU</b>, this value must be initialized to <b>NULL</b> prior to calling this method because, in most cases, this is a marshalled call. Not initializing this variable results in the marshaller attempting to access random memory.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu">ITfMenu</a>



<a href="/windows/desktop/TSF/tf-lbmenuf--constants">TF_LBMENUF_* Constants
      </a>