---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Remove
title: IFaxOutboundRoutingRules::Remove (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::Remove method removes an outbound routing rule (FaxOutboundRoutingRule object) from the FaxOutboundRoutingRules collection using the routing rule's index.
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7bs5.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],Remove method, IFaxOutboundRoutingRules.Remove, IFaxOutboundRoutingRules::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.remove, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp, fax._mfax_faxoutboundroutingrules_remove, faxcomex/IFaxOutboundRoutingRules::Remove
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
 - IFaxOutboundRoutingRules.Remove
 - IFaxOutboundRoutingRules.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutboundRoutingRules::Remove


## -description


The <b>IFaxOutboundRoutingRules::Remove</b> method removes an outbound routing rule (<a href="https://msdn.microsoft.com/en-us/library/ms690230(v=VS.85).aspx">FaxOutboundRoutingRule</a> object) from the <a href="https://msdn.microsoft.com/en-us/library/ms689525(v=VS.85).aspx">FaxOutboundRoutingRules</a> collection using the routing rule's index.


## -parameters




### -param lIndex

Type: <b>long</b>

A <b>long</b> value that specifies the index of the outbound routing rule to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of rules returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms687550(v=VS.85).aspx">IFaxOutboundRoutingRules::get_Count</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default outbound routing rule cannot be removed.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms689525(v=VS.85).aspx">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689527(v=VS.85).aspx">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693486(v=VS.85).aspx">Visual Basic Example</a>
 

 

