---
UID: NF:faxcomex.IFaxDeviceIds.Remove
title: IFaxDeviceIds::Remove (faxcomex.h)
author: windows-sdk-content
description: The IFaxDeviceIds::Remove method removes an item from the FaxDeviceIds collection.
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4m3p.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],Remove method, IFaxDeviceIds.Remove, IFaxDeviceIds::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxDeviceIds interface, _mfax_faxdeviceids.remove, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_remove_cpp, fax._mfax_faxdeviceids_remove, faxcomex/IFaxDeviceIds::Remove
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
 - IFaxDeviceIds.Remove
 - IFaxDeviceIds.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxDeviceIds::Remove


## -description


The <b>IFaxDeviceIds::Remove</b> method removes an item from the <a href="https://msdn.microsoft.com/en-us/library/ms686501(v=VS.85).aspx">FaxDeviceIds</a> collection.


## -parameters




### -param lIndex [in]

Type: <b>long</b>

A <b>long</b> value that specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms686492(v=VS.85).aspx">IFaxDeviceIds::get_Count</a> property.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  You cannot remove devices from the special <b>All Devices</b> routing group.</div>
<div> </div>
To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686501(v=VS.85).aspx">FaxDeviceIds</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686503(v=VS.85).aspx">IFaxDeviceIds</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693408(v=VS.85).aspx">Visual Basic Example</a>
 

 

