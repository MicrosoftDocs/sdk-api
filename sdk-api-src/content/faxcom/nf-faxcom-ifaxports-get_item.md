---
UID: NF:faxcom.IFaxPorts.get_Item
title: IFaxPorts::get_Item
author: windows-sdk-content
description: The IFaxPorts::get_Item method creates a FaxPort object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.
old-location: fax\_mfax_ifaxports_get_item.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0i0d.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IFaxPorts interface [Fax Service],get_Item method, IFaxPorts.get_Item, IFaxPorts::get_Item, _mfax_ifaxports_get_item, fax._mfax_ifaxports_get_item, faxcom/IFaxPorts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxPorts interface
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPorts.get_Item
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPorts::get_Item


## -description


The <b>IFaxPorts::get_Item</b> method creates a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax port to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax ports returned by a call to the <a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a>



<a href="https://msdn.microsoft.com/ac1e4c87-ba3b-4b49-887c-ed392ddab455">FaxPorts</a>



<a href="https://msdn.microsoft.com/e10c4f3e-c8bd-4134-a325-fe7da93b1caa">GetPorts</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/57736284-43f4-4ac3-bb43-313e6ee4ea44">IFaxPorts::get_Count</a>
 

 

