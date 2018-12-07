---
UID: NF:textserv.ITextHost.OnTxParaFormatChange
title: ITextHost::OnTxParaFormatChange
author: windows-sdk-content
description: Sets the default paragraph format for the text host.
old-location: controls\ITextHost_OnTxParaFormatChange.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxparaformatchange.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextHost interface [Windows Controls],OnTxParaFormatChange method, ITextHost.OnTxParaFormatChange, ITextHost::OnTxParaFormatChange, OnTxParaFormatChange, OnTxParaFormatChange method [Windows Controls], OnTxParaFormatChange method [Windows Controls],ITextHost interface, _win32_ITextHost_OnTxParaFormatChange, _win32_ITextHost_OnTxParaFormatChange_cpp, controls.ITextHost_OnTxParaFormatChange, controls._win32_ITextHost_OnTxParaFormatChange, textserv/ITextHost::OnTxParaFormatChange
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
 - ITextHost.OnTxParaFormatChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::OnTxParaFormatChange


## -description


Sets the default paragraph format for the text host.


## -parameters




### -param pPF [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb787940(v=VS.85).aspx">PARAFORMAT</a>*</b>

The new default paragraph format. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK if the method succeeds. 

Return one of the following COM error codes if the method fails. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>. 

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




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787615(v=VS.85).aspx">ITextHost</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787940(v=VS.85).aspx">PARAFORMAT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787609(v=VS.85).aspx">Windowless Rich Edit Controls</a>
 

 

