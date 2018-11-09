---
UID: NF:faxcomex.IFaxOutboundRoutingRules.Remove
title: IFaxOutboundRoutingRules::Remove
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::Remove method removes an outbound routing rule (FaxOutboundRoutingRule object) from the FaxOutboundRoutingRules collection using the routing rule's index.
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7bs5.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],Remove method, IFaxOutboundRoutingRules.Remove, IFaxOutboundRoutingRules::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.remove, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_remove_cpp, fax._mfax_faxoutboundroutingrules_remove, faxcomex/IFaxOutboundRoutingRules::Remove
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
 - IFaxOutboundRoutingRules.Remove
 - IFaxOutboundRoutingRules.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingRules::Remove


## -description


The <b>IFaxOutboundRoutingRules::Remove</b> method removes an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) from the <a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a> collection using the routing rule's index.


## -parameters




### -param lIndex

Type: <b>long</b>

A <b>long</b> value that specifies the index of the outbound routing rule to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of rules returned by a call to the <a href="https://msdn.microsoft.com/3add9157-b82a-4046-ad20-f6a29f92257e">IFaxOutboundRoutingRules::get_Count</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default outbound routing rule cannot be removed.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/35bb803d-fce4-46a3-825a-ec3a5138ed67">Visual Basic Example</a>
 

 

