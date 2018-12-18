---
UID: NF:faxcomex.IFaxIncomingMessage2.ReAssign
title: IFaxIncomingMessage2::ReAssign
author: windows-sdk-content
description: Reassign the fax to one or more recipients. It also commits changes to the IFaxIncomingMessage2::Subject, IFaxIncomingMessage2::SenderName, IFaxIncomingMessage2::SenderFaxNumber, and IFaxIncomingMessage2::HasCoverPage properties.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_reassign_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\reassign.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Reassign method, IFaxIncomingMessage2.ReAssign, IFaxIncomingMessage2.Reassign, IFaxIncomingMessage2::ReAssign, IFaxIncomingMessage2::Reassign, ReAssign, Reassign method [Fax Service], Reassign method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.reassign, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_reassign_cpp, fax._mfax_faxincomingmessage_reassign, faxcomex/IFaxIncomingMessage2::Reassign
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
 - IFaxIncomingMessage2.Reassign
 - IFaxIncomingMessage2.Reassign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::ReAssign


## -description



<a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">Reassign</a> the fax to one or more recipients. It also commits changes to the <a href="https://msdn.microsoft.com/en-us/library/Aa359006(v=VS.85).aspx">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359005(v=VS.85).aspx">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359004(v=VS.85).aspx">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa358996(v=VS.85).aspx">IFaxIncomingMessage2::HasCoverPage</a> properties.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_RECEIVE_FOLDER</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access rights. Also, IFaxConfiguration::IncomingFaxesArePublic must be set to false.

If the <a href="https://msdn.microsoft.com/en-us/library/Aa358860(v=VS.85).aspx">routing assistant</a> application is going to set the <a href="https://msdn.microsoft.com/en-us/library/Aa359006(v=VS.85).aspx">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359005(v=VS.85).aspx">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359004(v=VS.85).aspx">IFaxIncomingMessage2::SenderFaxNumber</a>, or <a href="https://msdn.microsoft.com/en-us/library/Aa358996(v=VS.85).aspx">IFaxIncomingMessage2::HasCoverPage</a> properties, it should do this before calling <b>IFaxIncomingMessage2::Reassign</b>. <b>Reassign</b> will commit those changes, so it is not necessary to call <a href="https://msdn.microsoft.com/en-us/library/Aa359003(v=VS.85).aspx">IFaxIncomingMessage2::Save</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

