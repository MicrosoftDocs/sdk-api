---
UID: NF:faxcomex.IFaxDevices.get_Item
title: IFaxDevices::get_Item
author: windows-sdk-content
description: The IFaxDevices::get_Item method returns a FaxDevice object from the FaxDevices collection, using its index.
old-location: fax\_mfax_faxdevices_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5j8t_cpp.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxDevices interface [Fax Service],get_Item method, IFaxDevices.get_Item, IFaxDevices::get_Item, _mfax_faxdevices.item_cpp, fax._mfax_faxdevices_item_cpp, faxcomex/IFaxDevices::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxDevices interface
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
 - IFaxDevices.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevices::get_Item


## -description


The <b>IFaxDevices::get_Item</b> method returns a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection, using its index.


## -parameters




### -param vIndex [in]

Type: <b>VARIANT</b>

<b>VARIANT</b> that specifies the index of the item to retrieve from the fax device collection. If this parameter is type VT_I2 or VT_I4, the parameter specifies the index of the item to retrieve from the collection. Valid values for the index are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="https://msdn.microsoft.com/44a0bbbb-7f5f-41de-9331-e473c155faaf">IFaxDevices::get_Count</a> method. If this parameter is type VT_BSTR, the parameter is a string containing the unique name of the fax device to retrieve. Other types are not supported.


### -param pFaxDevice [out]

Type: <b><a href="https://msdn.microsoft.com/3f4f4e83-df62-43af-903c-0b816bade3b9">IFaxDevice</a>**</b>

Receives the address of a pointer to a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To retrieve an item from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection using the device ID, call the <a href="https://msdn.microsoft.com/74863134-1ab8-49fc-ad59-f147ca8bdb45">IFaxDevices::get_ItemById</a> property.




## -see-also




<a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a>



<a href="https://msdn.microsoft.com/64bdc08c-1902-448a-9eda-b557ab4bb095">Visual Basic Example</a>
 

 

