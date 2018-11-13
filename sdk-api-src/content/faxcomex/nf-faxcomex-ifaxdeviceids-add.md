---
UID: NF:faxcomex.IFaxDeviceIds.Add
title: IFaxDeviceIds::Add
author: windows-sdk-content
description: The IFaxDeviceIds::Add method adds a fax device to the FaxDeviceIds collection, using the device's ID.
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4g2s.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxDeviceIds interface, IFaxDeviceIds interface [Fax Service],Add method, IFaxDeviceIds.Add, IFaxDeviceIds::Add, _mfax_faxdeviceids.add, fax._mfax_faxdeviceids_add, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_add_cpp, faxcomex/IFaxDeviceIds::Add
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
 - IFaxDeviceIds.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDeviceIds::Add


## -description


The <b>IFaxDeviceIds::Add</b> method adds a fax device to the <a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a> collection, using the device's ID.


## -parameters




### -param lDeviceId [in]

Type: <b>long</b>

A <b>long</b> value that specifies the ID of the fax device to add to the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method can also return remote procedure call (RPC) return values. For more information, see <a href="_rpc_rpc_return_values">RPC Return Values</a>.

<div class="alert"><b>Note</b>  You cannot add devices to the special <b>All Devices</b> routing group. Also, you can only add valid device IDs. You can obtain the valid ID of a device in the <a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a> collection through the <a href="https://msdn.microsoft.com/84e54535-4b40-4572-b8e1-3ab5095dbd6a">Id</a> property.</div>
<div> </div>
To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/a1906ca1-0025-464a-bb60-752b25c802e7">FaxDeviceIds</a>



<a href="https://msdn.microsoft.com/8ba11f07-3796-4910-98f7-541a32519c41">IFaxDeviceIds</a>



<a href="https://msdn.microsoft.com/5a05df3b-c56b-4dfc-a0ee-7f1c2861e9ae">Visual Basic Example</a>
 

 

