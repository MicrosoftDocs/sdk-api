---
UID: NF:faxcom.IFaxRoutingMethods.get_Count
title: IFaxRoutingMethods::get_Count (faxcom.h)
author: windows-sdk-content
description: The IFaxRoutingMethods::get_Count returns the number of fax routing methods associated with a FaxPort object.
old-location: fax\_mfax_ifaxroutingmethods_get_count.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0lis.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxRoutingMethods interface [Fax Service],get_Count method, IFaxRoutingMethods.get_Count, IFaxRoutingMethods::get_Count, _mfax_ifaxroutingmethods_get_count, fax._mfax_ifaxroutingmethods_get_count, faxcom/IFaxRoutingMethods::get_Count, get_Count, get_Count method [Fax Service], get_Count method [Fax Service],IFaxRoutingMethods interface
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


The <b>IFaxRoutingMethods::get_Count</b> returns the number of fax routing methods associated with a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object.


## -parameters




### -param pVal [out]

Type: <b>LONG*</b>

A pointer to a <b>LONG</b> that receives the number of routing methods associated with this fax port. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



After calling the <b>IFaxRoutingMethods::get_Count</b> method, a fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms692331(v=VS.85).aspx">IFaxRoutingMethods::get_Item</a> method to retrieve interface pointers to one or more <a href="https://msdn.microsoft.com/en-us/library/ms691842(v=VS.85).aspx">FaxRoutingMethod</a> objects.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691943(v=VS.85).aspx">GetRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691856(v=VS.85).aspx">IFaxRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692291(v=VS.85).aspx">IFaxRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692331(v=VS.85).aspx">IFaxRoutingMethods::get_Item</a>
 

 

