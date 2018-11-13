---
UID: NF:faxcom.IFaxRoutingMethods.get_Count
title: IFaxRoutingMethods::get_Count
author: windows-sdk-content
description: The IFaxRoutingMethods::get_Count returns the number of fax routing methods associated with a FaxPort object.
old-location: fax\_mfax_ifaxroutingmethods_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0lis.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Count method, IFaxRoutingMethods.get_Count, IFaxRoutingMethods::get_Count, _mfax_ifaxroutingmethods_get_count, fax._mfax_ifaxroutingmethods_get_count, faxcom/IFaxRoutingMethods::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxRoutingMethods interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxRoutingMethods.get_Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethods::get_Count


## -description


The <b>IFaxRoutingMethods::get_Count</b> returns the number of fax routing methods associated with a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.


## -parameters




### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of routing methods associated with this fax port. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>IFaxRoutingMethods::get_Count</b> method, a fax client application can call the <a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">IFaxRoutingMethods::get_Item</a> method to retrieve interface pointers to one or more <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> objects.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">GetRoutingMethods</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>



<a href="https://msdn.microsoft.com/403ba8dc-6faa-4067-b77a-9c451baa8a33">IFaxRoutingMethods::get_Item</a>
 

 

