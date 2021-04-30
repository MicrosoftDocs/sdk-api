---
UID: NF:segment.IMSVidOutputDevices.get__NewEnum
title: IMSVidOutputDevices::get__NewEnum (segment.h)
description: The get__NewEnum method retrieves an enumerator for the collection.
helpviewer_keywords: ["IMSVidOutputDevices interface [Microsoft TV Technologies]","get__NewEnum method","IMSVidOutputDevices.get__NewEnum","IMSVidOutputDevices::get__NewEnum","IMSVidOutputDevicesget__NewEnum","get__NewEnum","get__NewEnum method [Microsoft TV Technologies]","get__NewEnum method [Microsoft TV Technologies]","IMSVidOutputDevices interface","mstv.imsvidoutputdevices_get__newenum","segment/IMSVidOutputDevices::get__NewEnum"]
old-location: mstv\imsvidoutputdevices_get__newenum.htm
tech.root: mstv
ms.assetid: 2f2203bb-9367-4713-8369-06002a5842e9
ms.date: 12/05/2018
ms.keywords: IMSVidOutputDevices interface [Microsoft TV Technologies],get__NewEnum method, IMSVidOutputDevices.get__NewEnum, IMSVidOutputDevices::get__NewEnum, IMSVidOutputDevicesget__NewEnum, get__NewEnum, get__NewEnum method [Microsoft TV Technologies], get__NewEnum method [Microsoft TV Technologies],IMSVidOutputDevices interface, mstv.imsvidoutputdevices_get__newenum, segment/IMSVidOutputDevices::get__NewEnum
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidOutputDevices::get__NewEnum
 - segment/IMSVidOutputDevices::get__NewEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidOutputDevices.get__NewEnum
---

# IMSVidOutputDevices::get__NewEnum


## -description

The <b>get__NewEnum</b> method retrieves an enumerator for the collection.

## -parameters

### -param pD [out]

Pointer to a variable that receives an <b>IEnumVARIANT</b> interface pointer.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

This method is provided so that Automation clients can iterate through the collection using a <code>For...Each</code> loop.

The returned <b>IEnumVARIANT</b> interface is not thread safe, because it is intended primarily for use by Automation clients. Clients should not call methods on the interface from more than one thread. (C++ applications should generally use the <a href="/windows/desktop/api/segment/nf-segment-imsvidoutputdevices-get_item">IMSVidOutputDevices::get_Item</a> method instead.)

If the method succeeds, the <b>IEnumVARIANT</b> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidoutputdevices">IMSVidOutputDevices Interface</a>