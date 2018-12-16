---
UID: NF:faxcom.IFaxRoutingMethods.get_Item
title: IFaxRoutingMethods::get_Item
author: windows-sdk-content
description: The IFaxRoutingMethods::get_Item method creates a FaxRoutingMethod object for a specified fax routing method. The object allows enumeration of fax routing information for a specified FaxPort object.
old-location: fax\_mfax_ifaxroutingmethods_get_item.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7kq5.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Item method, IFaxRoutingMethods.get_Item, IFaxRoutingMethods::get_Item, _mfax_ifaxroutingmethods_get_item, fax._mfax_ifaxroutingmethods_get_item, faxcom/IFaxRoutingMethods::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxRoutingMethods interface
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
 - IFaxRoutingMethods.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxRoutingMethods::get_Item


## -description


The <b>IFaxRoutingMethods::get_Item</b> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object for a specified fax routing method. The object allows enumeration of fax routing information for a specified <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax routing method to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax routing methods returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms690829(v=VS.85).aspx">IFaxRoutingMethods::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxRoutingMethod</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691943(v=VS.85).aspx">GetRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690829(v=VS.85).aspx">IFaxRoutingMethods::get_Count</a>
 

 

