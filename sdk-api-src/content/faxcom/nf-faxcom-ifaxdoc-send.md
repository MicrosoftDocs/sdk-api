---
UID: NF:faxcom.IFaxDoc.Send
title: IFaxDoc::Send
author: windows-sdk-content
description: The Send method transmits the document specified by the FileName property of a FaxDoc object. The method can send the fax to the fax number specified by the FaxNumber property.
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_send_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8o2s.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxDoc interface [Fax Service],Send method, IFaxDoc.Send, IFaxDoc::Send, Send, Send method [Fax Service], Send method [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_send, fax._mfax_ifaxdoc_mfax_ifaxdoc_send_cpp, fax._mfax_ifaxdoc_send, faxcom/IFaxDoc::Send
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxDoc.Send
 - IFaxDoc.Send
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDoc::Send


## -description


The <b>Send</b> method transmits the document specified by the <a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">FileName</a> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The method can send the fax to the fax number specified by the <a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">FaxNumber</a> property.


## -parameters




### -param pVal [out, retval]

Type: <b>LONG*</b>

Specifies a pointer to a variable to receive a unique number that identifies the queued job that will send the fax transmission.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/fe9f0c64-7722-49ca-809c-5e59acacf474">FileName</a> property is required to send a fax transmission using a call to the <b>IFaxDoc::Send</b> method. The <a href="https://msdn.microsoft.com/462ce14c-3440-4e01-919b-9587c19c31a4">FaxNumber</a> property is also required. For more information, see <a href="https://msdn.microsoft.com/bee4d50b-d6e3-432b-9db6-c7df837079f4">Transmitting Faxes</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>
 

 

