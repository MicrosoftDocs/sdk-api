---
UID: NF:textserv.ITextHost.TxGetPasswordChar
title: ITextHost::TxGetPasswordChar (textserv.h)
author: windows-sdk-content
description: Requests the text host's password character.
old-location: controls\ITextHost_TxGetPasswordChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetpasswordchar.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetPasswordChar method, ITextHost.TxGetPasswordChar, ITextHost::TxGetPasswordChar, TxGetPasswordChar, TxGetPasswordChar method [Windows Controls], TxGetPasswordChar method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetPasswordChar, _win32_ITextHost_TxGetPasswordChar_cpp, controls.ITextHost_TxGetPasswordChar, controls._win32_ITextHost_TxGetPasswordChar, textserv/ITextHost::TxGetPasswordChar
ms.topic: method
f1_keywords: 
 - "textserv/ITextHost.TxGetPasswordChar"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextHost::TxGetPasswordChar


## -description


Requests the text host's password character.


## -parameters




### -param pch [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">TCHAR</a>*</b>

The password character. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Return S_OK if the password character is enabled. 

Return S_FALSE if the password character is not enabled. For more information on COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>. 




## -remarks



The password character is only shown if the TXTBIT_USEPASSWORD bit is enabled in the text services object. If the password character changes, re-enable the TXTBIT_USEPASSWORD bit through <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textserv/nf-textserv-itextservices-ontxpropertybitschange">OnTxPropertyBitsChange</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
 

 

