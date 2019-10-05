---
UID: NF:textserv.ITextHost.OnTxCharFormatChange
title: ITextHost::OnTxCharFormatChange (textserv.h)
author: windows-sdk-content
description: Sets the default character format for the text host.
old-location: controls\ITextHost_OnTxCharFormatChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxcharformatchange.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],OnTxCharFormatChange method, ITextHost.OnTxCharFormatChange, ITextHost::OnTxCharFormatChange, OnTxCharFormatChange, OnTxCharFormatChange method [Windows Controls], OnTxCharFormatChange method [Windows Controls],ITextHost interface, _win32_ITextHost_OnTxCharFormatChange, _win32_ITextHost_OnTxCharFormatChange_cpp, controls.ITextHost_OnTxCharFormatChange, controls._win32_ITextHost_OnTxCharFormatChange, textserv/ITextHost::OnTxCharFormatChange
ms.topic: method
f1_keywords: 
 - "textserv/ITextHost.OnTxCharFormatChange"
dev_langs:
 - c++
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
 - ITextHost.OnTxCharFormatChange
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost::OnTxCharFormatChange


## -description


Sets the default character format for the text host.


## -parameters




### -param pCF [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/win32/api/richedit/ns-richedit-charformata">CHARFORMAT</a>*</b>

The new default-character format. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return one of the following COM error codes if the method fails. For more information on COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>. 

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
One or more arguments are not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/richedit/ns-richedit-charformata">CHARFORMAT</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
 

 

