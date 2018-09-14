---
UID: NF:textserv.ITextHost.OnTxCharFormatChange
title: ITextHost::OnTxCharFormatChange
author: windows-sdk-content
description: Sets the default character format for the text host.
old-location: controls\ITextHost_OnTxCharFormatChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxcharformatchange.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITextHost interface [Windows Controls],OnTxCharFormatChange method, ITextHost.OnTxCharFormatChange, ITextHost::OnTxCharFormatChange, OnTxCharFormatChange, OnTxCharFormatChange method [Windows Controls], OnTxCharFormatChange method [Windows Controls],ITextHost interface, _win32_ITextHost_OnTxCharFormatChange, _win32_ITextHost_OnTxCharFormatChange_cpp, controls.ITextHost_OnTxCharFormatChange, controls._win32_ITextHost_OnTxCharFormatChange, textserv/ITextHost::OnTxCharFormatChange
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
 - ITextHost.OnTxCharFormatChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextHost::OnTxCharFormatChange


## -description


Sets the default character format for the text host.


## -parameters




### -param pCF [in]

Type: <b>const <a href="https://msdn.microsoft.com/7b31e42a-5e9b-46bf-9c4e-fd223c34a076">CHARFORMAT</a>*</b>

The new default-character format. 


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




<a href="https://msdn.microsoft.com/7b31e42a-5e9b-46bf-9c4e-fd223c34a076">CHARFORMAT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

