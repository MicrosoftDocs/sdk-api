---
UID: NF:faxcomex.IFaxOutgoingMessage.Delete
title: IFaxOutgoingMessage::Delete
author: windows-sdk-content
description: The IFaxOutgoingMessage::Delete method deletes the fax message from the outbound archive.
old-location: fax\_mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_delete_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_06w5.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Delete, Delete method [Fax Service], Delete method [Fax Service],IFaxOutgoingMessage interface, IFaxOutgoingMessage interface [Fax Service],Delete method, IFaxOutgoingMessage.Delete, IFaxOutgoingMessage::Delete, _mfax_faxoutgoingmessage.delete, fax._mfax_faxoutgoingmessage_cpp_mfax_faxoutgoingmessage_delete_cpp, fax._mfax_faxoutgoingmessage_delete, faxcomex/IFaxOutgoingMessage::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IFaxOutgoingMessage.Delete
 - IFaxOutgoingMessage.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage::Delete


## -description


The <b>IFaxOutgoingMessage::Delete</b> method deletes the fax message from the outbound archive.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> or <b>farMANAGE_OUT_ARCHIVE</b> access right.

With the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farSUBMIT_LOW</a> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_OUT_ARCHIVE</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690152(v=VS.85).aspx">IFaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693402(v=VS.85).aspx">Visual Basic Example</a>
 

 

