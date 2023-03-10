---
UID: NF:faxcomex.IFaxDeviceIds.Remove
title: IFaxDeviceIds::Remove (faxcomex.h)
description: The IFaxDeviceIds::Remove method removes an item from the FaxDeviceIds collection.
helpviewer_keywords: ["IFaxDeviceIds interface [Fax Service]","Remove method","IFaxDeviceIds.Remove","IFaxDeviceIds::Remove","Remove","Remove method [Fax Service]","Remove method [Fax Service]","IFaxDeviceIds interface","_mfax_faxdeviceids.remove","fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_remove_cpp","fax._mfax_faxdeviceids_remove","faxcomex/IFaxDeviceIds::Remove"]
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_remove_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4m3p.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],Remove method, IFaxDeviceIds.Remove, IFaxDeviceIds::Remove, Remove, Remove method [Fax Service], Remove method [Fax Service],IFaxDeviceIds interface, _mfax_faxdeviceids.remove, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_remove_cpp, fax._mfax_faxdeviceids_remove, faxcomex/IFaxDeviceIds::Remove
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxDeviceIds::Remove
 - faxcomex/IFaxDeviceIds::Remove
dev_langs:
 - c++
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
---

# IFaxDeviceIds::Remove


## -description

The <b>IFaxDeviceIds::Remove</b> method removes an item from the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

## -parameters

### -param lIndex [in]

Type: <b>long</b>

A <b>long</b> value that specifies the index of the item to remove from the collection. Valid values for this parameter are in the range from 1 to n, where n is the number of devices returned by a call to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids-count-vb">IFaxDeviceIds::get_Count</a> property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  You cannot remove devices from the special <b>All Devices</b> routing group.</div>
<div> </div>
To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>