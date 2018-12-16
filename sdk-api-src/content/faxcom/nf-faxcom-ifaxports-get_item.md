---
UID: NF:faxcom.IFaxPorts.get_Item
title: IFaxPorts::get_Item
author: windows-sdk-content
description: The IFaxPorts::get_Item method creates a FaxPort object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.
old-location: fax\_mfax_ifaxports_get_item.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0i0d.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxPorts interface [Fax Service],get_Item method, IFaxPorts.get_Item, IFaxPorts::get_Item, _mfax_ifaxports_get_item, fax._mfax_ifaxports_get_item, faxcom/IFaxPorts::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxPorts interface
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
 - IFaxPorts.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxPorts::get_Item


## -description


The <b>IFaxPorts::get_Item</b> method creates a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object for a specified fax port. The object allows enumeration of port configuration information for a specific connection to a fax server.


## -parameters




### -param Index [in]

Type: <b>LONG</b>

Specifies a <b>LONG</b> variable that indicates the fax port to retrieve. Valid values for this parameter are in the range from 1 to <i>n</i>, where <i>n</i> is the number of fax ports returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms692338(v=VS.85).aspx">IFaxPorts::get_Count</a> method. 


### -param pVal [out]

Type: <b>VARIANT*</b>

Receives a pointer to a <b>VARIANT</b> structure that receives an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The method returns a <b>ppdispVal</b> member with a VT_DISPATCH data type.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A fax client application can also access the <a href="https://msdn.microsoft.com/en-us/library/ms691281(v=VS.85).aspx">IFaxPort</a> interface directly by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxPort</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691338(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692319(v=VS.85).aspx">FaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692815(v=VS.85).aspx">GetPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692338(v=VS.85).aspx">IFaxPorts::get_Count</a>
 

 

