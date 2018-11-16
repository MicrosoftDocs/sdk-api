---
UID: NF:textserv.ITextHost.TxGetPasswordChar
title: ITextHost::TxGetPasswordChar
author: windows-sdk-content
description: Requests the text host's password character.
old-location: controls\ITextHost_TxGetPasswordChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetpasswordchar.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetPasswordChar method, ITextHost.TxGetPasswordChar, ITextHost::TxGetPasswordChar, TxGetPasswordChar, TxGetPasswordChar method [Windows Controls], TxGetPasswordChar method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetPasswordChar, _win32_ITextHost_TxGetPasswordChar_cpp, controls.ITextHost_TxGetPasswordChar, controls._win32_ITextHost_TxGetPasswordChar, textserv/ITextHost::TxGetPasswordChar
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
 - ITextHost.TxGetPasswordChar
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- textserv.h
: 
- ITextHost.TxGetPasswordChar
: 
---

# ITextHost::TxGetPasswordChar


## -description


Requests the text host's password character.


## -parameters




### -param pch [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">TCHAR</a>*</b>

The password character. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK if the password character is enabled. 

Return S_FALSE if the password character is not enabled. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>. 




## -remarks



The password character is only shown if the TXTBIT_USEPASSWORD bit is enabled in the text services object. If the password character changes, re-enable the TXTBIT_USEPASSWORD bit through <a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<a href="https://msdn.microsoft.com/41ae1a84-e721-4666-bac0-eb11c9b55279">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

