---
UID: NF:imm.ImmGetImeMenuItemsW
title: ImmGetImeMenuItemsW function (imm.h)
description: The ImmGetImeMenuItemsW (Unicode) function (imm.h) retrieves the menu items that are registered in the IME menu of a specified input context.
helpviewer_keywords: ["IGIMIF_RIGHTMENU", "IGIMII_CMODE", "IGIMII_CONFIGURE", "IGIMII_HELP", "IGIMII_INPUTTOOLS", "IGIMII_OTHER", "IGIMII_SMODE", "IGIMII_TOOLS", "ImmGetImeMenuItems", "ImmGetImeMenuItems function [Internationalization for Windows Applications]", "ImmGetImeMenuItemsW", "_win32_ImmGetImeMenuItems", "imm/ImmGetImeMenuItems", "imm/ImmGetImeMenuItemsW", "intl.immgetimemenuitems"]
old-location: intl\immgetimemenuitems.htm
tech.root: Intl
ms.assetid: 452c864d-b2e7-452a-85f2-d06d46170865
ms.date: 08/04/2022
ms.keywords: IGIMIF_RIGHTMENU, IGIMII_CMODE, IGIMII_CONFIGURE, IGIMII_HELP, IGIMII_INPUTTOOLS, IGIMII_OTHER, IGIMII_SMODE, IGIMII_TOOLS, ImmGetImeMenuItems, ImmGetImeMenuItems function [Internationalization for Windows Applications], ImmGetImeMenuItemsA, ImmGetImeMenuItemsW, _win32_ImmGetImeMenuItems, imm/ImmGetImeMenuItems, imm/ImmGetImeMenuItemsA, imm/ImmGetImeMenuItemsW, intl.immgetimemenuitems
req.header: imm.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ImmGetImeMenuItemsW (Unicode) and ImmGetImeMenuItemsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmGetImeMenuItemsW
 - imm/ImmGetImeMenuItemsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imm32.dll
api_name:
 - ImmGetImeMenuItems
 - ImmGetImeMenuItemsA
 - ImmGetImeMenuItemsW
---

## -description

Retrieves the menu items that are registered in the IME menu of a specified input context.

## -parameters

### -param unnamedParam1 [in]

Handle to the input context for the specified menu items.

### -param unnamedParam2 [in]

Flag specifying menu information options. The following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IGIMIF_RIGHTMENU"></a><a id="igimif_rightmenu"></a><dl>
<dt><b>IGIMIF_RIGHTMENU</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items for the context menu, obtained by a right mouse click.

</td>
</tr>
</table>

### -param unnamedParam3 [in]

Type of menu to retrieve. This parameter can have one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IGIMII_CMODE"></a><a id="igimii_cmode"></a><dl>
<dt><b>IGIMII_CMODE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control conversion mode.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_SMODE"></a><a id="igimii_smode"></a><dl>
<dt><b>IGIMII_SMODE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control sentence mode.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_CONFIGURE"></a><a id="igimii_configure"></a><dl>
<dt><b>IGIMII_CONFIGURE</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that are related to IME configuration.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_TOOLS"></a><a id="igimii_tools"></a><dl>
<dt><b>IGIMII_TOOLS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that are related to IME tools.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_HELP"></a><a id="igimii_help"></a><dl>
<dt><b>IGIMII_HELP</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control IME Help.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_OTHER"></a><a id="igimii_other"></a><dl>
<dt><b>IGIMII_OTHER</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control other IME functions.

</td>
</tr>
<tr>
<td width="40%"><a id="IGIMII_INPUTTOOLS"></a><a id="igimii_inputtools"></a><dl>
<dt><b>IGIMII_INPUTTOOLS</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the menu items that control menu items related to IME input tools providing an extended way to input characters.

</td>
</tr>
</table>

### -param lpImeParentMenu [out, optional]

Pointer to an <a href="/windows/desktop/api/imm/ns-imm-imemenuiteminfoa">IMEMENUITEMINFO</a> structure in which the function retrieves parent menu information. To retrieve information about the submenu items of this parent menu, the application sets the <b>fType</b> member to MFT_SUBMENU. This parameter contains <b>NULL</b> if the function retrieves only top-level menu items.

### -param lpImeMenu [out, optional]

Pointer to an array of <a href="/windows/desktop/api/imm/ns-imm-imemenuiteminfoa">IMEMENUITEMINFO</a> structures in which the function retrieves information about the menu items. This parameter contains <b>NULL</b> if the function retrieves the number of registered menu items.

### -param dwSize [in]

Size of the buffer to receive the <a href="/windows/desktop/api/imm/ns-imm-imemenuiteminfoa">IMEMENUITEMINFO</a> structure.

## -returns

Returns the number of menu items copied into <i>lpImeMenu</i>. If <i>lpImeMenu</i> specifies <b>NULL</b>, the function returns the number of registered menu items in the specified input context.

## -see-also

<a href="/windows/desktop/api/imm/ns-imm-imemenuiteminfoa">IMEMENUITEMINFO</a>



<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>

## -remarks

> [!NOTE]
> The imm.h header defines ImmGetImeMenuItems as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
