---
UID: NF:faxcomex.IFaxDeviceIds.get_Item
title: IFaxDeviceIds::get_Item
author: windows-sdk-content
description: The IFaxDeviceIds::get_Item method represents a device ID from the FaxDeviceIds collection.
old-location: fax\_mfax_faxdeviceids_item_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_0xt9_cpp.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],get_Item method, IFaxDeviceIds.get_Item, IFaxDeviceIds::get_Item, _mfax_faxdeviceids.item_cpp, fax._mfax_faxdeviceids_item_cpp, faxcomex/IFaxDeviceIds::get_Item, get_Item, get_Item method [Fax Service], get_Item method [Fax Service],IFaxDeviceIds interface
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
 - IFaxDeviceIds.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDeviceIds::get_Item


## -description


The <b>IFaxDeviceIds::get_Item</b> method represents a device ID from the <a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a> collection.


## -parameters




### -param lIndex [in]

Type: <b>long</b>

A value specifying the item to retrieve from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="https://msdn.microsoft.com/d47b51e0-d228-467b-acb3-b84e3cebb76d">IFaxDeviceIds::get_Count</a> method.


### -param plDeviceId [out, retval]

Type: <b>long*</b>

Pointer to a value that receives the item requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a>



<a href="https://msdn.microsoft.com/8ba11f07-3796-4910-98f7-541a32519c41">IFaxDeviceIds</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

