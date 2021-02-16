---
UID: NF:mswmdm.IWMDMStorage3.SetEnumPreference
title: IWMDMStorage3::SetEnumPreference (mswmdm.h)
description: The SetEnumPreference method sets the preferred view mode for the storage.
helpviewer_keywords: ["IWMDMStorage3 interface [windows Media Device Manager]","SetEnumPreference method","IWMDMStorage3.SetEnumPreference","IWMDMStorage3::SetEnumPreference","IWMDMStorage3SetEnumPreference","SetEnumPreference","SetEnumPreference method [windows Media Device Manager]","SetEnumPreference method [windows Media Device Manager]","IWMDMStorage3 interface","mswmdm/IWMDMStorage3::SetEnumPreference","wmdm.iwmdmstorage3_setenumpreference"]
old-location: wmdm\iwmdmstorage3_setenumpreference.htm
tech.root: WMDM
ms.assetid: 74916098-07d2-4dc9-932d-b174a10032dd
ms.date: 12/05/2018
ms.keywords: IWMDMStorage3 interface [windows Media Device Manager],SetEnumPreference method, IWMDMStorage3.SetEnumPreference, IWMDMStorage3::SetEnumPreference, IWMDMStorage3SetEnumPreference, SetEnumPreference, SetEnumPreference method [windows Media Device Manager], SetEnumPreference method [windows Media Device Manager],IWMDMStorage3 interface, mswmdm/IWMDMStorage3::SetEnumPreference, wmdm.iwmdmstorage3_setenumpreference
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMStorage3::SetEnumPreference
 - mswmdm/IWMDMStorage3::SetEnumPreference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage3.SetEnumPreference
---

# IWMDMStorage3::SetEnumPreference


## -description

The <b>SetEnumPreference</b> method sets the preferred view mode for the storage.

## -parameters

### -param pMode [in, out]

Desired mode of the storage enumerator. For more details on the mode, see <a href="/windows/desktop/WMDM/wmdm-storage-enum-mode">WMDM_STORAGE_ENUM_MODE</a>. If the value of <i>pMode</i> is set to ENUM_MODE_USE_DEVICE_PREF, then upon return it is set to ENUM_MODE_RAW or ENUM_MODE_METADATA_VIEWS, based on the device preference.

### -param nViews [in]

Number of view definitions provided.

This parameter is ignored if the value of <i>pMode</i> is ENUM_MODE_RAW or if the value of <i>pMode</i> is ENUM_MODE_USE_DEVICE_PREF and the device does not prefer metadata views.

If the value of <i>pMode</i> is ENUM_MODE_METADATA_VIEWS or if the value of <i>pMode</i> is ENUM_MODE_USE_DEVICE_PREF and the device prefers metadata views, this parameter can still be 0. In this case, Windows Media Device Manager uses its default metadata views.

If the value of <i>nViews</i> is 0, <i>ppViews</i> must be <b>NULL</b>. If the value of <i>nViews</i> is not 0, <i>ppViews</i> must point to an array of <a href="/windows/desktop/WMDM/wmdmmetadataview">WMDMMetadataView</a> structures with <i>nViews</i> elements.

### -param pViews [in]

Array of view definitions. The length of the array must be equal to <i>nViews</i>.

This parameter is ignored if the value of <i>pMode</i> is ENUM_MODE_RAW or if the value of <i>pMode</i> is ENUM_MODE_USE_DEVICE_PREF and the device does not prefer metadata views.

If the value of <i>pMode</i> is ENUM_MODE_METADATA_VIEWS or if the value of <i>pMode</i> is ENUM_MODE_USE_DEVICE_PREF and the device prefers metadata views, this parameter can still be <b>NULL</b>. In this case Windows Media Device Manager uses its default metadata views.

The value of this parameter must be <b>NULL</b> if the value of <i>nViews</i> is 0. If the value of <i>nViews</i> is not 0, <i>ppViews</i> must point to an array of <a href="/windows/desktop/WMDM/wmdmmetadataview">WMDMMetadataView</a> structures with <i>nViews</i> elements.

## -returns

The method returns an <b>HRESULT</b>. The following table lists all possible values.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to allocate the item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOT_CERTIFIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the rights to execute this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

Windows Media Device Manager can present metadata views of the content on the device. It walks through all the content on a top-level storage (such as internal memory or a storage card) and returns a storage enumerator that presents the content organized by the metadata of the content. The definition of a metadata view is provided through a <a href="/windows/desktop/WMDM/wmdmmetadataview">WMDMMetadataView</a> structure.

This behavior is controlled by the <i>pMode</i> parameter. If the <i>pMode</i> is set to ENUM_MODE_RAW, Windows Media Device Manager returns an enumerator that mirrors the hierarchy of the file system on the storage of the device. If the <i>pMode</i> is set to ENUM_MODE_METADATA_VIEWS, Windows Media Device Manager generates metadata views.

Devices indicate their preference by setting the device parameter <i>UseMetadataViews</i> at the time the device is installed. For more information about <i>UseMetadataViews</i>, see <a href="/windows/desktop/WMDM/device-parameters">Device Parameters</a>. If the application will let the device decide on the kind of storage enumerator returned, it should set <i>pMode</i> to ENUM_MODE_USE_DEVICE_PREF.

After this method is called, later calls to <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a> will behave according to the storage enumeration preference set by this method. This method can be called again to change the behavior of subsequent <b>IWMDMStorage::EnumStorage</b> calls.

This method should typically be called on the top-level storage. If this method is called on any of the storages in metadata view, it will return WMDM_E_NOTSUPPORTED.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata">IWMDMMetaData Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage">IWMDMStorage Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage">IWMDMStorage::EnumStorage</a>



<a href="/windows/desktop/WMDM/wmdmmetadataview">WMDMMetadataView</a>