---
UID: NF:faxcomex.IFaxDeviceIds.SetOrder
title: IFaxDeviceIds::SetOrder (faxcomex.h)
description: The IFaxDeviceIds::SetOrder method changes the order of a device in the ordered FaxDeviceIds collection.
helpviewer_keywords: ["IFaxDeviceIds interface [Fax Service]","SetOrder method","IFaxDeviceIds.SetOrder","IFaxDeviceIds::SetOrder","SetOrder","SetOrder method [Fax Service]","SetOrder method [Fax Service]","IFaxDeviceIds interface","_mfax_faxdeviceids.setorder","fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_setorder_cpp","fax._mfax_faxdeviceids_setorder","faxcomex/IFaxDeviceIds::SetOrder"]
old-location: fax\_mfax_faxdeviceids_cpp_mfax_faxdeviceids_setorder_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_4nci.htm
ms.date: 12/05/2018
ms.keywords: IFaxDeviceIds interface [Fax Service],SetOrder method, IFaxDeviceIds.SetOrder, IFaxDeviceIds::SetOrder, SetOrder, SetOrder method [Fax Service], SetOrder method [Fax Service],IFaxDeviceIds interface, _mfax_faxdeviceids.setorder, fax._mfax_faxdeviceids_cpp_mfax_faxdeviceids_setorder_cpp, fax._mfax_faxdeviceids_setorder, faxcomex/IFaxDeviceIds::SetOrder
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
 - IFaxDeviceIds::SetOrder
 - faxcomex/IFaxDeviceIds::SetOrder
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
 - IFaxDeviceIds.SetOrder
 - IFaxDeviceIds.SetOrder
---

# IFaxDeviceIds::SetOrder


## -description

The <b>IFaxDeviceIds::SetOrder</b> method changes the order of a device in the ordered <a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a> collection.

## -parameters

### -param lDeviceId [in]

Type: <b>long</b>

Specifies the device ID of the device whose order you want to change.

### -param lNewOrder [in]

Type: <b>long</b>

Specifies the new position of the device in the order.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You identify the device with its device ID, and then choose a new place for it in the order. If you move the device closer to the top of the order, the devices below that position in the order will drop down to accommodate the change. If you move the device closer to the bottom of the order, the devices above that position in the order will move up to fill the gap caused by the change.

In a fax device group, the relative order of the devices within the group is significant. When the fax service initiates an outgoing job, it attempts to select the first fax device in the device group. If that device is not available, the service selects the next available device that follows in rank order, and so on. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-groups">Fax Device Groups</a>.

To use this method, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farMANAGE_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxdeviceids">FaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxdeviceids">IFaxDeviceIds</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-managing-outbound-routing-groups">Visual Basic Example</a>