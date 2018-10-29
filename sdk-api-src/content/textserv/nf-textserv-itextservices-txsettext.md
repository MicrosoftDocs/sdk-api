---
UID: NF:textserv.ITextServices.TxSetText
title: ITextServices::TxSetText
author: windows-sdk-content
description: Sets all of the text in the control.
old-location: controls\ITextServices_TxSetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txsettext.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITextServices interface [Windows Controls],TxSetText method, ITextServices.TxSetText, ITextServices::TxSetText, TxSetText, TxSetText method [Windows Controls], TxSetText method [Windows Controls],ITextServices interface, _win32_ITextServices_TxSetText, _win32_ITextServices_TxSetText_cpp, controls.ITextServices_TxSetText, controls._win32_ITextServices_TxSetText, textserv/ITextServices::TxSetText
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices.TxSetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextServices::TxSetText


## -description


Sets all of the text in the control.


## -parameters




### -param pszText [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The string which will replace the current text. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If the method fails, the return value is the following <b>HRESULT</b> code. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Text could not be updated.

</td>
</tr>
</table>
 




## -remarks



This method should be used with care; it essentially reinitializes the text services object with some new data. Any previous data and formatting information will be lost, including undo information.

If previous data has been copied to the clipboard, that data will be rendered completely to the clipboard (through <a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>) before it is discarded.

This method does <i>not</i> support <b>Undo</b>.

Two alternate approaches to setting text are <a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a> and <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/b0bc844f-2d20-4e67-84c5-0a5313bf6dee">ITextServices</a>



<a href="https://msdn.microsoft.com/18291a91-be7d-42ec-a44a-d1bbfb017c6e">OleFlushClipboard</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">SetText</a>



<a href="https://msdn.microsoft.com/1b48c309-6903-4139-bf42-e8526963e681">WM_SETTEXT</a>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

