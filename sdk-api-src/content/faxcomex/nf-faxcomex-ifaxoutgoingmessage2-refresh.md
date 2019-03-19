---
UID: NF:faxcomex.IFaxOutgoingMessage2.Refresh
title: IFaxOutgoingMessage2::Refresh (faxcomex.h)
author: windows-sdk-content
description: Refreshes FaxOutgoingMessage object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
old-location: fax\_mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\refresh.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingMessage2 interface [Fax Service],Refresh method, IFaxOutgoingMessage2.Refresh, IFaxOutgoingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingMessage2 interface, _mfax_faxoutgoingmessage.refresh, fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp, fax._mfax_faxoutgoingmessage_refresh, faxcomex/IFaxOutgoingMessage2::Refresh
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
 - IFaxOutgoingMessage2.Refresh
 - IFaxOutgoingMessage2.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingMessage2::Refresh


## -description


Refreshes <a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/Aa358990(v=VS.85).aspx">Save</a> method call are lost.


<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690149(v=VS.85).aspx">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358984(v=VS.85).aspx">IFaxOutgoingMessage2</a>
 

 

