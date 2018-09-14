---
UID: NF:faxcomex.IFaxOutgoingMessage2.Refresh
title: IFaxOutgoingMessage2::Refresh
author: windows-sdk-content
description: Refreshes FaxOutgoingMessage object information from the fax server. When the Refresh method is called, any configuration changes made after the last Save method call are lost.
old-location: fax\_mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxoutgoingmessage2\refresh.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFaxOutgoingMessage2 interface [Fax Service],Refresh method, IFaxOutgoingMessage2.Refresh, IFaxOutgoingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingMessage2 interface, _mfax_faxoutgoingmessage.refresh, fax._mfax_faxoutgoingmessage2_cpp_mfax_faxoutgoingmessage_refresh_cpp, fax._mfax_faxoutgoingmessage_refresh, faxcomex/IFaxOutgoingMessage2::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
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


Refreshes <a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/e0492e6e-db3e-449c-b58b-ff365d80d5f7">Save</a> method call are lost.


<div class="alert"><b>Note</b>  This method is supported only on Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/fb06254f-f37b-4783-b4fd-42b5c5a28496">FaxOutgoingMessage</a>



<a href="https://msdn.microsoft.com/c6468db0-ea8d-4460-b389-43608337bd96">IFaxOutgoingMessage2</a>
 

 

