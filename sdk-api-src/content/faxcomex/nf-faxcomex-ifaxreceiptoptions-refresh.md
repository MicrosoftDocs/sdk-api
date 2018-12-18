---
UID: NF:faxcomex.IFaxReceiptOptions.Refresh
title: IFaxReceiptOptions::Refresh
author: windows-sdk-content
description: The IFaxReceiptOptions::Refresh method refreshes FaxReceiptOptions object information from the fax server. When the IFaxReceiptOptions::Refresh method is called, any configuration changes made after the last IFaxReceiptOptions::Save method call are lost.
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6xt4.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],Refresh method, IFaxReceiptOptions.Refresh, IFaxReceiptOptions::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.refresh, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_refresh_cpp, fax._mfax_faxreceiptoptions_refresh, faxcomex/IFaxReceiptOptions::Refresh
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
 - IFaxReceiptOptions.Refresh
 - IFaxReceiptOptions.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxReceiptOptions::Refresh


## -description


The <b>IFaxReceiptOptions::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> object information from the fax server. When the <b>IFaxReceiptOptions::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms688388(v=VS.85).aspx">IFaxReceiptOptions::Save</a> method call are lost.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690119(v=VS.85).aspx">IFaxReceiptOptions</a>
 

 

