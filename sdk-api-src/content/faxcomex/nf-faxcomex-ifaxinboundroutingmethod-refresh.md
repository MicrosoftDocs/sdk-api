---
UID: NF:faxcomex.IFaxInboundRoutingMethod.Refresh
title: IFaxInboundRoutingMethod::Refresh
author: windows-sdk-content
description: The IFaxInboundRoutingMethod::Refresh method refreshes IFaxInboundRoutingMethod interface information from the fax server.
old-location: fax\_mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_42aw.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IFaxInboundRoutingMethod interface [Fax Service],Refresh method, IFaxInboundRoutingMethod.Refresh, IFaxInboundRoutingMethod::Refresh, Refresh, Refresh method [Fax Service], Refresh method [Fax Service],IFaxInboundRoutingMethod interface, _mfax_faxinboundroutingmethod.refresh, fax._mfax_faxinboundroutingmethod_cpp_mfax_faxinboundroutingmethod_refresh_cpp, fax._mfax_faxinboundroutingmethod_refresh, faxcomex/IFaxInboundRoutingMethod::Refresh
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
 - IFaxInboundRoutingMethod.Refresh
 - IFaxInboundRoutingMethod.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxInboundRoutingMethod::Refresh


## -description


The <b>IFaxInboundRoutingMethod::Refresh</b> method refreshes <a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a> interface information from the fax server.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the <b>IFaxInboundRoutingMethod::Refresh</b> method is called, any configuration changes made after the last <a href="https://msdn.microsoft.com/7fd645f1-9162-46ea-89a9-0888d86ec187">IFaxInboundRoutingMethod::Save</a> method call are lost.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/8eb68201-4c87-41ce-a401-a039b5ad454d">FaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/ca33c439-24e7-4b85-8e29-a0a0176f0ae2">IFaxInboundRoutingMethod</a>



<a href="https://msdn.microsoft.com/cef24608-cab1-4090-aa94-3a1b76733e98">Visual Basic Example</a>
 

 

