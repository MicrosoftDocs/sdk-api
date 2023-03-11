---
UID: NF:vdshwprv.IVdsProvider.GetProperties
title: IVdsProvider::GetProperties (vdshwprv.h)
description: The IVdsProvider::GetProperties (vdshwprv.h) method returns the properties of a provider.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsProvider interface","IVdsProvider interface [VDS]","GetProperties method","IVdsProvider.GetProperties","IVdsProvider::GetProperties","base.ivdsprovider_getproperties","vds/IVdsProvider::GetProperties","vdshwprv/IVdsProvider::GetProperties"]
old-location: base\ivdsprovider_getproperties.htm
tech.root: base
ms.assetid: a4cb18c5-2cda-4d0a-9be0-4a548ec2f6eb
ms.date: 08/08/2022
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsProvider interface, IVdsProvider interface [VDS],GetProperties method, IVdsProvider.GetProperties, IVdsProvider::GetProperties, base.ivdsprovider_getproperties, vds/IVdsProvider::GetProperties, vdshwprv/IVdsProvider::GetProperties
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVdsProvider::GetProperties
 - vdshwprv/IVdsProvider::GetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProvider.GetProperties
---

# IVdsProvider::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the 
   properties of a provider.

## -parameters

### -param pProviderProp [out]

The address of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a> 
      structure allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszName</b> and <b>pwszVersion</b> member strings. Callers must free 
      the strings by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -returns

This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>VDS_S_PROPERTIES_INCOMPLETE</b></b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsprovider">IVdsProvider</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a>
