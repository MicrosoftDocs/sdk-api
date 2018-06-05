---
UID: NF:textserv.ITextServices.OnTxPropertyBitsChange
title: ITextServices::OnTxPropertyBitsChange
author: windows-sdk-content
description: Sets properties (represented by bits) for the control.
old-location: controls\ITextServices_OnTxPropertyBitsChange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxpropertybitschange.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ITextServices interface [Windows Controls],OnTxPropertyBitsChange method, ITextServices.OnTxPropertyBitsChange, ITextServices::OnTxPropertyBitsChange, OnTxPropertyBitsChange, OnTxPropertyBitsChange method [Windows Controls], OnTxPropertyBitsChange method [Windows Controls],ITextServices interface, TXTBIT_ALLOWBEEP, TXTBIT_AUTOWORDSEL, TXTBIT_BACKSTYLECHANGE, TXTBIT_CHARFORMATCHANGE, TXTBIT_CLIENTRECTCHANGE, TXTBIT_D2DDWRITE, TXTBIT_D2DPIXELSNAPPED, TXTBIT_D2DSIMPLETYPOGRAPHY, TXTBIT_D2DSUBPIXELLINES, TXTBIT_DISABLEDRAG, TXTBIT_EXTENTCHANGE, TXTBIT_HIDESELECTION, TXTBIT_MAXLENGTHCHANGE, TXTBIT_MULTILINE, TXTBIT_NOTHREADREFCOUNT, TXTBIT_PARAFORMATCHANGE, TXTBIT_READONLY, TXTBIT_RICHTEXT, TXTBIT_SAVESELECTION, TXTBIT_SCROLLBARCHANGE, TXTBIT_SELBARCHANGE, TXTBIT_SHOWACCELERATOR, TXTBIT_SHOWPASSWORD, TXTBIT_USECURRENTBKG, TXTBIT_USEPASSWORD, TXTBIT_VERTICAL, TXTBIT_VIEWINSETCHANGE, TXTBIT_WORDWRAP, _win32_ITextServices_OnTxPropertyBitsChange, _win32_ITextServices_OnTxPropertyBitsChange_cpp, controls.ITextServices_OnTxPropertyBitsChange, controls._win32_ITextServices_OnTxPropertyBitsChange, textserv/ITextServices::OnTxPropertyBitsChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextServices.OnTxPropertyBitsChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::OnTxPropertyBitsChange


## -description


Sets properties (represented by bits) for the control.


## -parameters




### -param dwMask [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Bits representing properties to be changed. For the possible bit values, see the TXTBIT_* values list in <i>dwBits</i>. 


### -param dwBits [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

New values for bit properties. It can be any combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_ALLOWBEEP"></a><a id="txtbit_allowbeep"></a><dl>
<dt><b>TXTBIT_ALLOWBEEP</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, beeping is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_AUTOWORDSEL"></a><a id="txtbit_autowordsel"></a><dl>
<dt><b>TXTBIT_AUTOWORDSEL</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the AutoWordSelect feature is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_BACKSTYLECHANGE"></a><a id="txtbit_backstylechange"></a><dl>
<dt><b>TXTBIT_BACKSTYLECHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the backstyle changed. See <a href="https://msdn.microsoft.com/03decbb6-b272-4ba0-a902-013aa0dde18e">TxGetBackStyle</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_CHARFORMATCHANGE"></a><a id="txtbit_charformatchange"></a><dl>
<dt><b>TXTBIT_CHARFORMATCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the character format changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_CLIENTRECTCHANGE"></a><a id="txtbit_clientrectchange"></a><dl>
<dt><b>TXTBIT_CLIENTRECTCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the client rectangle changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_DISABLEDRAG"></a><a id="txtbit_disabledrag"></a><dl>
<dt><b>TXTBIT_DISABLEDRAG</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, dragging is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_D2DDWRITE"></a><a id="txtbit_d2ddwrite"></a><dl>
<dt><b>TXTBIT_D2DDWRITE</b></dt>
</dl>
</td>
<td width="60%">
 Use Direct2D/DirectWrite for this instance, and not GDI/Uniscribe.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_D2DPIXELSNAPPED"></a><a id="txtbit_d2dpixelsnapped"></a><dl>
<dt><b>TXTBIT_D2DPIXELSNAPPED</b></dt>
</dl>
</td>
<td width="60%">
 Render glyphs to the nearest pixel positions. Valid only if D2DDWRITE is set.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_D2DSUBPIXELLINES"></a><a id="txtbit_d2dsubpixellines"></a><dl>
<dt><b>TXTBIT_D2DSUBPIXELLINES</b></dt>
</dl>
</td>
<td width="60%">
 Draw lines with subpixel precision. Don't pixel-snap text lines, underline, and strikethrough
												in the secondary text flow direction (usually vertical). Valid only if D2DDWRITE is set and D2DPIXELSNAPPED is not set.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_D2DSIMPLETYPOGRAPHY"></a><a id="txtbit_d2dsimpletypography"></a><dl>
<dt><b>TXTBIT_D2DSIMPLETYPOGRAPHY</b></dt>
</dl>
</td>
<td width="60%">
 Render text using simple typography (no glyph rendering). This value is valid only if TXTBIT_D2DDWRITE is also specified. 

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_EXTENTCHANGE"></a><a id="txtbit_extentchange"></a><dl>
<dt><b>TXTBIT_EXTENTCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the size of the client rectangle changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_HIDESELECTION"></a><a id="txtbit_hideselection"></a><dl>
<dt><b>TXTBIT_HIDESELECTION</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the text services object should hide the selection when the control is inactive. If <b>FALSE</b>, the selection should be displayed when the control is inactive.

Note, this implies <b>TXTBIT_SAVESELECTION</b> is <b>TRUE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_MAXLENGTHCHANGE"></a><a id="txtbit_maxlengthchange"></a><dl>
<dt><b>TXTBIT_MAXLENGTHCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the maximum length for text in the control changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_MULTILINE"></a><a id="txtbit_multiline"></a><dl>
<dt><b>TXTBIT_MULTILINE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the text services object should work in multiline mode. Use the <b>TXTBIT_WORDWRAP</b> value to determine whether to wrap the lines to the view rectangle or clip them.

If <b>FALSE</b>, the text services object should not process a carriage return/line feed from the ENTER key and it should truncate incoming text containing hard line breaks just before the first line break. It is also acceptable to truncate text that is set with <a href="https://msdn.microsoft.com/29be3eba-285c-4297-b692-0a5fcb4797c6">ITextServices::TxSetText</a>, because it is the responsibility of the host not to use a single-line control when bound to a multiline field.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_NOTHREADREFCOUNT"></a><a id="txtbit_nothreadrefcount"></a><dl>
<dt><b>TXTBIT_NOTHREADREFCOUNT</b></dt>
</dl>
</td>
<td width="60%">
 Don't reference TLS data on behalf of this instance.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_PARAFORMATCHANGE"></a><a id="txtbit_paraformatchange"></a><dl>
<dt><b>TXTBIT_PARAFORMATCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the paragraph format changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_READONLY"></a><a id="txtbit_readonly"></a><dl>
<dt><b>TXTBIT_READONLY</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the text services object should not accept any editing change through the user interface. However, it should still accept programmatic changes through <a href="https://msdn.microsoft.com/1ba9e4c0-7870-4057-8a8b-d0e6577349ac">EM_SETTEXTEX</a>, 	<a href="https://msdn.microsoft.com/525e6f5a-f52f-4bab-bc76-caa484729897">EM_REPLACESEL</a>, and <a href="https://msdn.microsoft.com/29be3eba-285c-4297-b692-0a5fcb4797c6">ITextServices::TxSetText</a>. Also, the user should still be able to move the insertion point, select text, and carry out other operations that don't modify content, such as Copy.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_RICHTEXT"></a><a id="txtbit_richtext"></a><dl>
<dt><b>TXTBIT_RICHTEXT</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the text services object should be in rich-text mode.

If <b>FALSE</b>, it is in plain-text mode.

Note, this affects how editing commands are applied. For example, applying bold to part of the text in a plain-edit control makes the entire text bold. However, for a rich-edit control, this makes only the selected text bold.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_SAVESELECTION"></a><a id="txtbit_saveselection"></a><dl>
<dt><b>TXTBIT_SAVESELECTION</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the boundaries of the selection should be saved when the control is inactive.

If <b>FALSE</b>, when the control goes active again the selection boundaries can be reset to start = 0, length = 0.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_SCROLLBARCHANGE"></a><a id="txtbit_scrollbarchange"></a><dl>
<dt><b>TXTBIT_SCROLLBARCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the scroll bar has changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_SELBARCHANGE"></a><a id="txtbit_selbarchange"></a><dl>
<dt><b>TXTBIT_SELBARCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the selection bar width has changed

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_SHOWACCELERATOR"></a><a id="txtbit_showaccelerator"></a><dl>
<dt><b>TXTBIT_SHOWACCELERATOR</b></dt>
</dl>
</td>
<td width="60%">
If set, the accelerator character should be underlined.

This must be set in order to call <a href="https://msdn.microsoft.com/c0658f73-edab-4540-a560-110e277b8d27">TxGetAcceleratorPos</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_SHOWPASSWORD"></a><a id="txtbit_showpassword"></a><dl>
<dt><b>TXTBIT_SHOWPASSWORD</b></dt>
</dl>
</td>
<td width="60%">
 Show password strings.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_USECURRENTBKG"></a><a id="txtbit_usecurrentbkg"></a><dl>
<dt><b>TXTBIT_USECURRENTBKG</b></dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_USEPASSWORD"></a><a id="txtbit_usepassword"></a><dl>
<dt><b>TXTBIT_USEPASSWORD</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, display text using the password character obtained by <a href="https://msdn.microsoft.com/f2208eca-13f7-4ba3-a642-9c66e7e89f59">TxGetPasswordChar</a>.

The notification on this property can mean either that the password character changed or that the password character was not used before but is used now (or vice versa).

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_VERTICAL"></a><a id="txtbit_vertical"></a><dl>
<dt><b>TXTBIT_VERTICAL</b></dt>
</dl>
</td>
<td width="60%">
Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_VIEWINSETCHANGE"></a><a id="txtbit_viewinsetchange"></a><dl>
<dt><b>TXTBIT_VIEWINSETCHANGE</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b>, the inset changed.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTBIT_WORDWRAP"></a><a id="txtbit_wordwrap"></a><dl>
<dt><b>TXTBIT_WORDWRAP</b></dt>
</dl>
</td>
<td width="60%">
If <b>TRUE</b> and TXTBIT_MULTILINE is also <b>TRUE</b>, multiline controls should wrap the line to the view rectangle. If this property is <b>FALSE</b> and <b>TXTBIT_MULTILINE</b> is <b>TRUE</b>, the lines should not be wrapped but clipped. The right side of the view rectangle should be ignored.

If <b>TXTBIT_MULTILINE</b> is <b>FALSE</b>, this property has no effect.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is the following <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> code. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
</table>
 




## -remarks



The client rectangle is the rectangle that the text services object is responsible for painting and managing. The host relies on the text services object for painting that area. The text services object must not paint or invalidate areas outside of that rectangle. In addition, the host will forward mouse messages to the text services object when the cursor is over this rectangle. This rectangle is expressed in client coordinates of the containing window.

The view inset is the amount of space on each side between the client rectangle and the view rectangle. The view rectangle (also called the Formatting rectangle) is the rectangle in which the text should be formatted. For more information, see <a href="https://msdn.microsoft.com/78f68d49-15b2-443a-a92a-d0c1c8d0e9e8">TxGetViewInset</a>.

The backstyle is the style of the background of the client rectangle. It can be either TXTBACK_TRANSPARENT or TXTBACK_SOLID. See <b>TXTBACKSTYLE</b>.

The scroll bar property indicates changes to the scroll bar: which scroll bar is present, whether scroll bars are hidden or disabled when scrolling is impossible, and also if auto-scrolling is enabled when the insertion point gets off the client rectangle.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/c0658f73-edab-4540-a560-110e277b8d27">TxGetAcceleratorPos</a>



<a href="https://msdn.microsoft.com/03decbb6-b272-4ba0-a902-013aa0dde18e">TxGetBackStyle</a>



<a href="https://msdn.microsoft.com/7b1d8dbf-73b7-4a0d-8bb0-14e506de6aaf">TxGetClientRect</a>



<a href="https://msdn.microsoft.com/f2208eca-13f7-4ba3-a642-9c66e7e89f59">TxGetPasswordChar</a>



<a href="https://msdn.microsoft.com/29be3eba-285c-4297-b692-0a5fcb4797c6">TxSetText</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

