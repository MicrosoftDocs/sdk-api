---
UID: NF:faxcomex.IFaxOutgoingArchive.Refresh
title: IFaxOutgoingArchive::Refresh
author: windows-sdk-content
description: The IFaxOutgoingArchive::Refresh method refreshes FaxOutgoingArchive object information from the fax server.
old-location: fax\_mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6hm0.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutgoingArchive interface [Fax Service],Refresh method, IFaxOutgoingArchive.Refresh, IFaxOutgoingArchive::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutgoingArchive interface, _mfax_faxoutgoingarchive.refresh, fax._mfax_faxoutgoingarchive_cpp_mfax_faxoutgoingarchive_refresh_cpp, fax._mfax_faxoutgoingarchive_refresh, faxcomex/IFaxOutgoingArchive::Refresh
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
 - IFaxOutgoingArchive.Refresh
 - IFaxOutgoingArchive.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingArchive::Refresh


## -description


The <b>IFaxOutgoingArchive::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a> object information from the fax server. When the <b>IFaxOutgoingArchive::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/fb4941f9-4170-4336-a26e-32ae009b1176">IFaxOutgoingArchive::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/ffed51b3-0a07-4667-8d8d-5054362489c4">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/6bd3eb63-512e-4774-9bb7-f99d1293f2f3">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/072eb2cc-7fd9-4f8e-8583-44384357e708">Visual Basic Example</a>
 

 

