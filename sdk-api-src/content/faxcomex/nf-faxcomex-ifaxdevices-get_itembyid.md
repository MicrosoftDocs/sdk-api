---
UID: NF:faxcomex.IFaxDevices.get_ItemById
title: IFaxDevices::get_ItemById
author: windows-sdk-content
description: The IFaxDevices::get_ItemById method returns a FaxDevice object from the FaxDevices collection, using its device ID.
old-location: fax\_mfax_faxdevices_itembyid.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4gmc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDevices interface [Fax Service],get_ItemById method, IFaxDevices.get_ItemById, IFaxDevices::get_ItemById, _mfax_faxdevices.itembyid, fax._mfax_faxdevices_itembyid, faxcomex/IFaxDevices::get_ItemById, get_ItemById, get_ItemById method [Fax Service], get_ItemById method [Fax Service],IFaxDevices interface
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FaxComex.h
api_name:
 - IFaxDevices.get_ItemById
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDevices::get_ItemById


## -description


The <b>IFaxDevices::get_ItemById</b> method returns a <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection, using its device ID.


## -parameters




### -param lId [in]

Type: <b>long</b>

The unique ID of the device to retrieve.


### -param ppFaxDevice [out, retval]

Type: <b>ppFaxDevice**</b>

A <a href="https://msdn.microsoft.com/bb54b793-98e1-4862-b887-48c25099ac6d">FaxDevice</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To retrieve an item from the <a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a> collection using the device's index, call the <a href="https://msdn.microsoft.com/2c8539a4-19e5-47a3-9375-f7adefcb72a4">Item</a> property.




## -see-also




<a href="https://msdn.microsoft.com/f04644e4-5e20-490d-847c-001ae2aa7fe5">FaxDevices</a>



<a href="https://msdn.microsoft.com/025b7393-b693-4d75-973a-4a058059eb22">IFaxDevices</a>



<a href="https://msdn.microsoft.com/8e0d5b13-2126-49a2-80b7-ae3a817496bd">Visual Basic Example</a>
 

 

