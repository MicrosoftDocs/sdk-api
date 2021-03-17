---
UID: NF:mmdeviceapi.IMMDeviceCollection.Item
title: IMMDeviceCollection::Item (mmdeviceapi.h)
description: The Item method retrieves a pointer to the specified item in the device collection.
helpviewer_keywords: ["IMMDeviceCollection interface [Core Audio]","Item method","IMMDeviceCollection.Item","IMMDeviceCollection::Item","IMMDeviceCollectionItem","Item","Item method [Core Audio]","Item method [Core Audio]","IMMDeviceCollection interface","coreaudio.immdevicecollection_item","mmdeviceapi/IMMDeviceCollection::Item"]
old-location: coreaudio\immdevicecollection_item.htm
tech.root: CoreAudio
ms.assetid: 98cb72fd-9422-44b4-a585-a1fed029a77f
ms.date: 12/05/2018
ms.keywords: IMMDeviceCollection interface [Core Audio],Item method, IMMDeviceCollection.Item, IMMDeviceCollection::Item, IMMDeviceCollectionItem, Item, Item method [Core Audio], Item method [Core Audio],IMMDeviceCollection interface, coreaudio.immdevicecollection_item, mmdeviceapi/IMMDeviceCollection::Item
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMMDeviceCollection::Item
 - mmdeviceapi/IMMDeviceCollection::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDeviceCollection.Item
---

# IMMDeviceCollection::Item


## -description

The <b>Item</b> method retrieves a pointer to the specified item in the device collection.

## -parameters

### -param nDevice [in]

The device number. If the collection contains <i>n</i> devices, the devices are numbered 0 to <i>n</i>– 1.

### -param ppDevice [out]

Pointer to a pointer variable into which the method writes the address of the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice</a> interface of the specified item in the device collection. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>Item</b> call fails,  <i>*ppDevice</i> is <b>NULL</b>.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>ppDevice</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nDevice</i> is not a valid device number.

</td>
</tr>
</table>

## -remarks

This method retrieves a pointer to the <b>IMMDevice</b> interface of the specified item in the device collection. Each item in the collection is an endpoint object that represents an audio endpoint device. The caller selects a device from the device collection by specifying the device number. For a collection of <i>n</i> devices, valid device numbers range from 0 to <i>n</i>– 1. To obtain a count of the devices in a collection, call the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-getcount">IMMDeviceCollection::GetCount</a> method.

For a code example that calls the <b>Item</b> method, see <a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevice">IMMDevice Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection">IMMDeviceCollection Interface</a>



<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevicecollection-getcount">IMMDeviceCollection::GetCount</a>