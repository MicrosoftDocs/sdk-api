---
UID: NF:faxcomex.IFaxOutboundRouting.GetRules
title: IFaxOutboundRouting::GetRules (faxcomex.h)
author: windows-sdk-content
description: The IFaxOutboundRouting::GetRules method retrieves an interface that represents a collection of outbound routing groups.
old-location: fax\_mfax_faxoutboundrouting_getrules_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_2v1v_cpp.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRules, GetRules method [Fax Service], GetRules method [Fax Service],IFaxOutboundRouting interface, IFaxOutboundRouting interface [Fax Service],GetRules method, IFaxOutboundRouting.GetRules, IFaxOutboundRouting::GetRules, _mfax_faxoutboundrouting.getrules_cpp, fax._mfax_faxoutboundrouting_getrules_cpp, faxcomex/IFaxOutboundRouting::GetRules
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
 - IFaxOutboundRouting.GetRules
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxOutboundRouting::GetRules


## -description


The <b>IFaxOutboundRouting::GetRules</b> method retrieves an interface that represents a collection of outbound routing groups.


## -parameters




### -param pFaxOutboundRoutingRules [out, retval]

Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a>**</b>

An address of a pointer that receives an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundroutingrules">IFaxOutboundRoutingRules</a> interface.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxoutboundrouting">IFaxOutboundRouting</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-creating-and-managing-outbound-routing-rules">Visual Basic Example</a>
 

 

