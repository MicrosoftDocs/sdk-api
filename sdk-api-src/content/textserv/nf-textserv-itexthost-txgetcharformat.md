---
UID: NF:textserv.ITextHost.TxGetCharFormat
title: ITextHost::TxGetCharFormat
author: windows-sdk-content
description: Requests the text host's default character format.
old-location: controls\ITextHost_TxGetCharFormat.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetcharformat.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetCharFormat method, ITextHost.TxGetCharFormat, ITextHost::TxGetCharFormat, TxGetCharFormat, TxGetCharFormat method [Windows Controls], TxGetCharFormat method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetCharFormat, _win32_ITextHost_TxGetCharFormat_cpp, controls.ITextHost_TxGetCharFormat, controls._win32_ITextHost_TxGetCharFormat, textserv/ITextHost::TxGetCharFormat
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
 - ITextHost.TxGetCharFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::TxGetCharFormat


## -description


Requests the text host's default character format.


## -parameters




### -param ppCF

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb787881(v=VS.85).aspx">CHARFORMAT</a>**</b>

The default character format. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return the following COM error code if the method fails. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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



The text host retains ownership of the <a href="https://msdn.microsoft.com/en-us/library/Bb787881(v=VS.85).aspx">CHARFORMAT</a> returned. However, the pointer returned must remain valid until the text host notifies the text services object through <a href="https://msdn.microsoft.com/en-us/library/Bb787627(v=VS.85).aspx">OnTxPropertyBitsChange</a> that the default character format has changed.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787881(v=VS.85).aspx">CHARFORMAT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787627(v=VS.85).aspx">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

