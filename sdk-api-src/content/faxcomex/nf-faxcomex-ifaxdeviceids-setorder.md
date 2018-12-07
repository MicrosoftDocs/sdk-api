---
UID: NF:faxcomex.IFaxDeviceIds.SetOrder
title: IFaxDeviceIds::SetOrder
author: windows-sdk-content
description: The IFaxDeviceIds::SetOrder method changes the order of a device in the ordered FaxDeviceIds collection.
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_setorder_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4nci.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],SetOrder method, IFaxDeviceIds.SetOrder, IFaxDeviceIds::SetOrder, SetOrder, SetOrder method [Fax Service], SetOrder method [Fax Service],IFaxDeviceIds interface, _mfax_faxdeviceids.setorder, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_setorder_cpp, fax._mfax_faxdeviceids_setorder, faxcomex/IFaxDeviceIds::SetOrder
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
 - IFaxDeviceIds.SetOrder
 - IFaxDeviceIds.SetOrder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDeviceIds::SetOrder


## -description


The <b>IFaxDeviceIds::SetOrder</b> method changes the order of a device in the ordered <a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a> collection.


## -parameters




### -param lDeviceId [in]

Type: <b>long</b>

Specifies the device ID of the device whose order you want to change.


### -param lNewOrder [in]

Type: <b>long</b>

Specifies the new position of the device in the order.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You identify the device with its device ID, and then choose a new place for it in the order. If you move the device closer to the top of the order, the devices below that position in the order will drop down to accommodate the change. If you move the device closer to the bottom of the order, the devices above that position in the order will move up to fill the gap caused by the change.

In a fax device group, the relative order of the devices within the group is significant. When the fax service initiates an outgoing job, it attempts to select the first fax device in the device group. If that device is not available, the service selects the next available device that follows in rank order, and so on. For more information, see <a href="https://msdn.microsoft.com/88598e24-6339-49d9-8887-7370aa402135">Fax Device Groups</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a>



<a href="https://msdn.microsoft.com/8ba11f07-3796-4910-98f7-541a32519c41">IFaxDeviceIds</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

