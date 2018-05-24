---
UID: NF:textserv.ITextHost.TxGetParaFormat
title: ITextHost::TxGetParaFormat
author: windows-driver-content
description: Requests the text host's default paragraph format.
old-location: controls\ITextHost_TxGetParaFormat.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgetparaformat.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetParaFormat method, ITextHost.TxGetParaFormat, ITextHost::TxGetParaFormat, TxGetParaFormat, TxGetParaFormat method [Windows Controls], TxGetParaFormat method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetParaFormat, _win32_ITextHost_TxGetParaFormat_cpp, controls.ITextHost_TxGetParaFormat, controls._win32_ITextHost_TxGetParaFormat, textserv/ITextHost::TxGetParaFormat
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextHost.TxGetParaFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextHost::TxGetParaFormat


## -description


Requests the text host's default paragraph format.


## -parameters




### -param ppPF

Type: <b>const <a href="https://msdn.microsoft.com/c384f3d6-8f2f-4c82-8a98-bc95d8e5828c">PARAFORMAT</a>**</b>

The default paragraph format. 


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



The host object retains ownership of the <a href="https://msdn.microsoft.com/c384f3d6-8f2f-4c82-8a98-bc95d8e5828c">PARAFORMAT</a> structure that is returned. However, the pointer returned must remain valid until the host notifies the text services object, through <a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>, that the default paragraph format has changed.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>



<a href="https://msdn.microsoft.com/c384f3d6-8f2f-4c82-8a98-bc95d8e5828c">PARAFORMAT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

