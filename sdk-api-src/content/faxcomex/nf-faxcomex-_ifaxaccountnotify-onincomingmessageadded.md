---
UID: NF:faxcomex._IFaxAccountNotify.OnIncomingMessageAdded
title: "_IFaxAccountNotify::OnIncomingMessageAdded"
author: windows-sdk-content
description: Called by the fax service when an incoming message is added to the inbound fax archive.
old-location: fax\_mfax_ifaxaccountnotify_onincomingmessageadded.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxaccountnotify\onincomingmessageadded.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxAccountNotify.OnIncomingMessageAdded, OnIncomingMessageAdded, OnIncomingMessageAdded method [Fax Service], OnIncomingMessageAdded method [Fax Service],_IFaxAccountNotify interface, _IFaxAccountNotify interface [Fax Service],OnIncomingMessageAdded method, _IFaxAccountNotify.OnIncomingMessageAdded, _IFaxAccountNotify::OnIncomingMessageAdded, _mfax_ifaxaccountnotify_onincomingmessageadded, fax._mfax_ifaxaccountnotify_onincomingmessageadded, faxcomex/_IFaxAccountNotify::OnIncomingMessageAdded
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - _IFaxAccountNotify.OnIncomingMessageAdded
 - IFaxAccountNotify.OnIncomingMessageAdded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# _IFaxAccountNotify::OnIncomingMessageAdded


## -description


Called by the fax service when an incoming message is added to the inbound fax archive.


## -parameters




### -param pFaxAccount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a>*</b>

An <a href="https://msdn.microsoft.com/en-us/library/Aa359058(v=VS.85).aspx">IFaxAccount</a> object.


### -param bstrMessageId [in]

Type: <b>BSTR</b>

A null-terminated string that contains the ID of the message added to the inbound fax archive.


### -param fAddedToReceiveFolder [in]

Type: <b>VARIANT_BOOL</b>

A value that indicates whether the message was successfully added to the received folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To implement this functionality in Visual Basic, select and implement the appropriate event procedure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa359031(v=VS.85).aspx">IFaxAccountNotify</a>
 

 

