---
UID: NF:vds.IVdsService.GetProperties
title: IVdsService::GetProperties (vds.h)
description: Returns the properties of VDS.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsService interface","IVdsService interface [VDS]","GetProperties method","IVdsService.GetProperties","IVdsService::GetProperties","base.ivdsservice_getproperties","vds/IVdsService::GetProperties"]
old-location: base\ivdsservice_getproperties.htm
tech.root: base
ms.assetid: fb5fe743-4833-400a-a8aa-8de886203190
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsService interface, IVdsService interface [VDS],GetProperties method, IVdsService.GetProperties, IVdsService::GetProperties, base.ivdsservice_getproperties, vds/IVdsService::GetProperties
req.header: vds.h
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
 - IVdsService::GetProperties
 - vds/IVdsService::GetProperties
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
 - IVdsService.GetProperties
---

# IVdsService::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the 
   properties of VDS.

## -parameters

### -param pServiceProp [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure 
      allocated and passed in by the caller. VDS allocates memory for the 
      <b>pwszVersion</b> member string. Callers must free the string by using the 
      <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_PROPERTIES_INCOMPLETE</b></dt>
<dt>0x00042715L</dt>
</dl>
</td>
<td width="60%">
Some but not all of the properties were successfully retrieved. Note that there are many possible reasons for failing to retrieve all properties, including device removal.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsservice">IVdsService</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a>