---
UID: NF:mswmdm.IWMDMDevice3.SetProperty
title: IWMDMDevice3::SetProperty (mswmdm.h)
description: The SetProperty method sets a specific device property, if it is writable.
helpviewer_keywords: ["IWMDMDevice3 interface [windows Media Device Manager]","SetProperty method","IWMDMDevice3.SetProperty","IWMDMDevice3::SetProperty","IWMDMDevice3SetProperty","SetProperty","SetProperty method [windows Media Device Manager]","SetProperty method [windows Media Device Manager]","IWMDMDevice3 interface","mswmdm/IWMDMDevice3::SetProperty","wmdm.iwmdmdevice3_setproperty"]
old-location: wmdm\iwmdmdevice3_setproperty.htm
tech.root: WMDM
ms.assetid: 39483d9a-0725-45fa-9d41-dbabd400b3bf
ms.date: 12/05/2018
ms.keywords: IWMDMDevice3 interface [windows Media Device Manager],SetProperty method, IWMDMDevice3.SetProperty, IWMDMDevice3::SetProperty, IWMDMDevice3SetProperty, SetProperty, SetProperty method [windows Media Device Manager], SetProperty method [windows Media Device Manager],IWMDMDevice3 interface, mswmdm/IWMDMDevice3::SetProperty, wmdm.iwmdmdevice3_setproperty
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
 - IWMDMDevice3::SetProperty
 - mswmdm/IWMDMDevice3::SetProperty
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
 - IWMDMDevice3.SetProperty
---

# IWMDMDevice3::SetProperty


## -description

The <b>SetProperty</b> method sets a specific device property, if it is writable.

## -parameters

### -param pwszPropName [in]

A wide character, null-terminated string name of the property to set. This overwrites any existing property with the same name. Once the application has made this call, it should free any dynamic memory using <b>PropVariantClear</b>. A list of standard property name constants is given in <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

### -param pValue [in]

Value of the property being set.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method sets the specified device property. To obtain the list of supported device properties, the client should query the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty">IWMDMDevice3::GetProperty</a> method for the <b>g_wszWMDMSupportedDeviceProperties</b> property.

For the list of device property names, see <a href="/windows/desktop/WMDM/metadata-constants">Metadata Constants</a>.

This method is similar to the <b>SetMetadata</b> method for storages, but this method can set only one property at one time.

Not all properties of the device can be set.

## -see-also

<a href="/windows/desktop/WMDM/enumerating-devices">Enumerating Devices</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3">IWMDMDevice3 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty">IWMDMDevice3::GetProperty</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata">IWMDMStorage3::SetMetadata</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata">IWMDMStorage4::GetSpecifiedMetadata</a>



<a href="/windows/desktop/WMDM/setting-metadata-on-a-file">Setting Metadata on a File</a>