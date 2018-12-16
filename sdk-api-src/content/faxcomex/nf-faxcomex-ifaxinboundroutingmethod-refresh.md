---
UID: NF:faxcomex.IFaxInboundRoutingMethod.Refresh
title: IFaxInboundRoutingMethod::Refresh
author: windows-sdk-content
description: The IFaxInboundRoutingMethod::Refresh method refreshes IFaxInboundRoutingMethod interface information from the fax server.
old-location: fax\_mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_42aw.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxInboundRoutingMethod interface [Fax Service],Refresh method, IFaxInboundRoutingMethod.Refresh, IFaxInboundRoutingMethod::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxInboundRoutingMethod interface, _mfax_faxinboundroutingmethod.refresh, fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp, fax._mfax_faxinboundroutingmethod_refresh, faxcomex/IFaxInboundRoutingMethod::Refresh
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
 - IFaxInboundRoutingMethod.Refresh
 - IFaxInboundRoutingMethod.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingMethod::Refresh


## -description


The <b>IFaxInboundRoutingMethod::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms687470(v=VS.85).aspx">IFaxInboundRoutingMethod</a> interface information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <b>IFaxInboundRoutingMethod::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms684815(v=VS.85).aspx">IFaxInboundRoutingMethod::Save</a> method call are lost.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687469(v=VS.85).aspx">FaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687470(v=VS.85).aspx">IFaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693492(v=VS.85).aspx">Visual Basic Example</a>
 

 

