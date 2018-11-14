---
UID: NF:faxcomex.IFaxIncomingMessage2.Refresh
title: IFaxIncomingMessage2::Refresh
author: windows-sdk-content
description: Refreshes FaxIncomingMessage object information from the fax server.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\refresh.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Refresh method, IFaxIncomingMessage2.Refresh, IFaxIncomingMessage2::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.refresh, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_refresh_cpp, fax._mfax_faxincomingmessage_refresh, faxcomex/IFaxIncomingMessage2::Refresh
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
 - IFaxIncomingMessage2.Refresh
 - IFaxIncomingMessage2.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcomex.h
: 
- IFaxIncomingMessage2.Refresh
: 
---

# IFaxIncomingMessage2::Refresh


## -description


Refreshes <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object information from the fax server. When the <b>Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/6778fa8e-6abb-40c3-92bc-cc98dd20fba4">Save</a> method call are lost, except for the properties that are committed with the <a href="https://msdn.microsoft.com/befff3bc-4489-4a63-b231-ff2974c760d1">IFaxIncomingMessage2::Reassign</a> method: <a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/dba0099d-bf47-47e0-8a83-39a2fe9f4793">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/304f722e-4ea6-472c-99c3-1b129d143dae">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/71bd6223-e5d3-453c-b747-9b0be9b074c6">IFaxIncomingMessage2::HasCoverPage</a>.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/b3dc429e-1470-4e7d-8cd5-9cadb0052051">IFaxIncomingMessage2</a>
 

 

