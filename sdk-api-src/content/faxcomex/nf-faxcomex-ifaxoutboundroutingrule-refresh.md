---
UID: NF:faxcomex.IFaxOutboundRoutingRule.Refresh
title: IFaxOutboundRoutingRule::Refresh
author: windows-sdk-content
description: The IFaxOutboundRoutingRule::Refresh method refreshes FaxOutboundRoutingRule object information from the fax server.
old-location: fax\_mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6s2w.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxOutboundRoutingRule interface [Fax Service],Refresh method, IFaxOutboundRoutingRule.Refresh, IFaxOutboundRoutingRule::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxOutboundRoutingRule interface, _mfax_faxoutboundroutingrule.refresh, fax._mfax_faxoutboundroutingrule_cpp_mfax_faxoutboundroutingrule_refresh_cpp, fax._mfax_faxoutboundroutingrule_refresh, faxcomex/IFaxOutboundRoutingRule::Refresh
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
 - IFaxOutboundRoutingRule.Refresh
 - IFaxOutboundRoutingRule.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingRule::Refresh


## -description


The <b>IFaxOutboundRoutingRule::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/en-us/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a> object information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <b>IFaxOutboundRoutingRule::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/en-us/library/ms687544(v=VS.85).aspx">IFaxOutboundRoutingRule::Save</a> method call are lost.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690232(v=VS.85).aspx">IFaxOutboundRoutingRule</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693486(v=VS.85).aspx">Visual Basic Example</a>
 

 

