---
UID: NF:faxcomex.IFaxOutboundRoutingRules.ItemByCountryAndArea
title: IFaxOutboundRoutingRules::ItemByCountryAndArea
author: windows-sdk-content
description: The IFaxOutboundRoutingRules::get_ItemByCountryAndArea method returns an outbound routing rule (FaxOutboundRoutingRule object) from the collection using the routing rule's country/region code and area code.
old-location: fax\_mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_itembycountryandarea_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_8plt.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxOutboundRoutingRules interface [Fax Service],ItemByCountryAndArea method, IFaxOutboundRoutingRules.ItemByCountryAndArea, IFaxOutboundRoutingRules::ItemByCountryAndArea, ItemByCountryAndArea, ItemByCountryAndArea method [Fax Service], ItemByCountryAndArea method [Fax Service],IFaxOutboundRoutingRules interface, _mfax_faxoutboundroutingrules.itembycountryandarea, fax._mfax_faxoutboundroutingrules_cpp_mfax_faxoutboundroutingrules_itembycountryandarea_cpp, fax._mfax_faxoutboundroutingrules_itembycountryandarea, faxcomex/IFaxOutboundRoutingRules::ItemByCountryAndArea
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
 - IFaxOutboundRoutingRules.ItemByCountryAndArea
 - IFaxOutboundRoutingRules.ItemByCountryAndArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutboundRoutingRules::ItemByCountryAndArea


## -description


The <b>IFaxOutboundRoutingRules::get_ItemByCountryAndArea</b> method returns an outbound routing rule (<a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object) from the collection using the routing rule's country/region code and area code.


## -parameters




### -param lCountryCode

Type: <b>long</b>

A <b>long</b> value that specifies the country/region code of the outbound routing rule to retrieve. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will return a rule for any country/region code. 


### -param lAreaCode

Type: <b>long</b>

A <b>long</b> value that specifies the area code of the outbound routing rule to retrieve. Specifying <a href="https://msdn.microsoft.com/f064751c-d8c3-4a59-bd2d-3fb1f297af90">frrcANY_CODE</a> will return a rule for any area code within the specified country/region code. 


### -param pFaxOutboundRoutingRule

TBD




#### - FaxOutboundRoutingRule

Type: <b><a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a>**</b>

A <a href="https://msdn.microsoft.com/e027093a-314c-4292-b591-29c2bc58c031">FaxOutboundRoutingRule</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/971819e1-a3cb-4e58-b533-fee15ccb4352">FaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/bd059904-b5b6-4485-a64e-0beaa4de7379">IFaxOutboundRoutingRules</a>



<a href="https://msdn.microsoft.com/35bb803d-fce4-46a3-825a-ec3a5138ed67">Visual Basic Example</a>
 

 

