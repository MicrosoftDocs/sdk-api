---
UID: NF:imapi2.IDiscMaster2.get__NewEnum
title: IDiscMaster2::get__NewEnum (imapi2.h)
description: Retrieves a list of the CD and DVD devices installed on the computer.
helpviewer_keywords: ["IDiscMaster2 interface [IMAPI]","get__NewEnum method","IDiscMaster2.get__NewEnum","IDiscMaster2::get__NewEnum","get__NewEnum","get__NewEnum method [IMAPI]","get__NewEnum method [IMAPI]","IDiscMaster2 interface","imapi.idiscmaster2_get__newenum","imapi2/IDiscMaster2::get__NewEnum"]
old-location: imapi\idiscmaster2_get__newenum.htm
tech.root: imapi
ms.assetid: f148a1c0-cb76-40e9-9749-a074f04c93e8
ms.date: 12/05/2018
ms.keywords: IDiscMaster2 interface [IMAPI],get__NewEnum method, IDiscMaster2.get__NewEnum, IDiscMaster2::get__NewEnum, get__NewEnum, get__NewEnum method [IMAPI], get__NewEnum method [IMAPI],IDiscMaster2 interface, imapi.idiscmaster2_get__newenum, imapi2/IDiscMaster2::get__NewEnum
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscMaster2::get__NewEnum
 - imapi2/IDiscMaster2::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscMaster2.get__NewEnum
---

# IDiscMaster2::get__NewEnum


## -description

Retrieves a list of the CD and DVD devices installed on the computer.

## -parameters

### -param ppunk [out]

An <b>IEnumVariant</b> interface that you use to enumerate the CD and DVD devices installed on the computer. The items of the enumeration are variants whose type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to retrieve the unique identifier of the device.

## -returns

S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements. The <i>celt</i> and <i>pceltFetched</i> parameters are defined by <b>IEnumVariant</b>.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -remarks

The enumeration is a snapshot of the devices on the computer at the time of the call and will not reflect devices that are added and removed. To receive notification when a device is added or removed from the computer, implement the <a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events">DDiscMaster2Events</a> interface.

To retrieve a single identifier, see the <a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_item">IDiscMaster2::get_Item</a> property.

The device identifier is guaranteed to be unique and static for a given device as recognized by Windows Plug and Play.  You can use the identifier as a key value for saving the user's default burner, and can also be used to cache other device-specific static information (for example, VendorID and ProductID) by an advanced application.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2">IDiscMaster2</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscmaster2-get_count">IDiscMaster2::get_Count</a>