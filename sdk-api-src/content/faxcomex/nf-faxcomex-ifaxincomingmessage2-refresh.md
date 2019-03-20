---
UID: NF:faxcomex.IFaxIncomingMessage2.Refresh
title: IFaxIncomingMessage2::Refresh (faxcomex.h)
author: windows-sdk-content
description: Refreshes FaxIncomingMessage object information from the fax server.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\refresh.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Refresh method, IFaxIncomingMessage2.Refresh, IFaxIncomingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.refresh, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp, fax._mfax_faxincomingmessage_refresh, faxcomex/IFaxIncomingMessage2::Refresh
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
 - IFaxIncomingMessage2.Refresh
 - IFaxIncomingMessage2.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::Refresh


## -description


Refreshes <a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/Aa359003(v=VS.85).aspx">Save</a> method call are lost, except for the properties that are committed with the <a href="https://msdn.microsoft.com/en-us/library/Aa358998(v=VS.85).aspx">IFaxIncomingMessage2::Reassign</a> method: <a href="https://msdn.microsoft.com/en-us/library/Aa359006(v=VS.85).aspx">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359005(v=VS.85).aspx">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359004(v=VS.85).aspx">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa358996(v=VS.85).aspx">IFaxIncomingMessage2::HasCoverPage</a>.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

