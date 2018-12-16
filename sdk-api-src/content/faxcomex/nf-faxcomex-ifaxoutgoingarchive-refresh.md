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


The <b>IFaxOutgoingArchive::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a> object information from the fax server. When the <b>IFaxOutgoingArchive::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms689213(v=VS.85).aspx">IFaxOutgoingArchive::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  In Windows Vista, Windows Server 2008, and later versions of Windows, this method is not supported and returns an error.</div>
<div> </div>
To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms688634(v=VS.85).aspx">FaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688636(v=VS.85).aspx">IFaxOutgoingArchive</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693402(v=VS.85).aspx">Visual Basic Example</a>
 

 

