---
UID: NF:faxcom.IFaxRoutingMethods.get_Item
title: IFaxRoutingMethods::get_Item
author: windows-sdk-content
description: The IFaxRoutingMethods::get_Item method creates a FaxRoutingMethod object for a specified fax routing method. The object allows enumeration of fax routing information for a specified FaxPort object.
old-location: fax\_mfax_ifaxroutingmethods_get_item.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7kq5.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Item method, IFaxRoutingMethods.get_Item, IFaxRoutingMethods::get_Item, _mfax_ifaxroutingmethods_get_item, fax._mfax_ifaxroutingmethods_get_item, faxcom/IFaxRoutingMethods::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxRoutingMethods interface
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: ShellWindowTypeConstants
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	IFaxRoutingMethods.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxRoutingMethods::get_Item


## -description


The <b>IFaxRoutingMethods::get_Item</b> method creates a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object for a specified fax routing method. The object allows enumeration of fax routing information for a specified <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax routing method to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax routing methods returned by a call to the <a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">IFaxRoutingMethods::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/d759d840-80a4-4e59-a8e6-1cc6adc399ce">FaxRoutingMethod</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxRoutingMethod</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/c180dbac-2aaa-4e8e-9b1f-b6314b47d229">GetRoutingMethods</a>



<a href="https://msdn.microsoft.com/d61fd93e-814f-465e-a021-f454e33d6baf">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/8dfab525-4eda-42b9-ac02-c8c25575d0aa">IFaxRoutingMethods</a>



<a href="https://msdn.microsoft.com/7bbcf3aa-7dba-4452-817c-bf21bc646790">IFaxRoutingMethods::get_Count</a>
 

 

