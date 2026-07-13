---
UID: NF:faxcomex.IFaxDeviceIds.Add
title: IFaxDeviceIds::Add (faxcomex.h)
description: The IFaxDeviceIds::Add method adds a fax device to the FaxDeviceIds collection, using the device's ID.
helpviewer_keywords: ["Add","Add method [Fax Service]","Add method [Fax Service]","IFaxDeviceIds interface","IFaxDeviceIds interface [Fax Service]","Add method","IFaxDeviceIds.Add","IFaxDeviceIds::Add","_mfax_faxdeviceids.add","fax._mfax_faxdeviceids_add","fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_add_cpp","faxcomex/IFaxDeviceIds::Add"]
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_add_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4g2s.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [Fax Service], Add method [Fax Service],IFaxDeviceIds interface, IFaxDeviceIds interface [Fax Service],Add method, IFaxDeviceIds.Add, IFaxDeviceIds::Add, _mfax_faxdeviceids.add, fax._mfax_faxdeviceids_add, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_add_cpp, faxcomex/IFaxDeviceIds::Add
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
 - IFaxDeviceIds::Add
 - faxcomex/IFaxDeviceIds::Add
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
 - IFaxDeviceIds.Add
---

# IFaxDeviceIds::Add


## -description

The <b>IFaxDeviceIds::Add</b> method adds a fax device to the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection, using the device's ID.

## -parameters

### -param lDeviceId [in]

Type: <b>long</b>

A <b>long</b> value that specifies the ID of the fax device to add to the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can also return remote procedure call (RPC) return values. For more information, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

<div class="alert"><b>Note</b>  You cannot add devices to the special <b>All Devices</b> routing group. Also, you can only add valid device IDs. You can obtain the valid ID of a device in the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection through the <a href="/previous-versions/windows/desktop/fax/-mfax-faxdevice-id-vb">Id</a> property.</div>
<div> </div>
To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>