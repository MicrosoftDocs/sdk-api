---
UID: NF:textserv.ITextServices.TxGetText
title: ITextServices::TxGetText
author: windows-sdk-content
description: Returns all of the Unicode plain text in the control as a BSTR.
old-location: controls\ITextServices_TxGetText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgettext.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetText method, ITextServices.TxGetText, ITextServices::TxGetText, TxGetText, TxGetText method [Windows Controls], TxGetText method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetText, _win32_ITextServices_TxGetText_cpp, controls.ITextServices_TxGetText, controls._win32_ITextServices_TxGetText, textserv/ITextServices::TxGetText
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextServices.TxGetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices::TxGetText


## -description


Returns all of the Unicode plain text in the control as a <b>BSTR</b>.


## -parameters




### -param pbstrText

Type: <b>BSTR
          *</b>

The Unicode plain text. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the text is successfully returned in the output argument, the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid <b>BSTR</b> pointer passed in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for copy of the text.

</td>
</tr>
</table>
 




## -remarks



The host (caller) takes ownership of the returned <b>BSTR</b>.

Other ways to retrieve plain text data are to use <a href="https://msdn.microsoft.com/en-us/library/ms632627(v=VS.85).aspx">WM_GETTEXT</a> or the Text Object Model (TOM) <a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a> method.

If there is no text in the control, the <b>BSTR</b> is allocated and 0x000D is returned in it.

The returned text will <i>not</i> necessarily be null-terminated.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787617(v=VS.85).aspx">ITextServices</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632627(v=VS.85).aspx">WM_GETTEXT</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

