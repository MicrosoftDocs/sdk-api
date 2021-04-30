---
UID: NF:vds.IVdsPack.GetProperties
title: IVdsPack::GetProperties (vds.h)
description: Returns the property details of a pack object.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsPack interface","IVdsPack interface [VDS]","GetProperties method","IVdsPack.GetProperties","IVdsPack::GetProperties","base.ivdspack_getproperties","vds/IVdsPack::GetProperties"]
old-location: base\ivdspack_getproperties.htm
tech.root: base
ms.assetid: 0793642c-1905-470c-a69f-8bf5f8bbe90d
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsPack interface, IVdsPack interface [VDS],GetProperties method, IVdsPack.GetProperties, IVdsPack::GetProperties, base.ivdspack_getproperties, vds/IVdsPack::GetProperties
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
 - IVdsPack::GetProperties
 - vds/IVdsPack::GetProperties
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
 - IVdsPack.GetProperties
---

# IVdsPack::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns the 
   property details of a pack object.

## -parameters

### -param pPackProp [out]

The address of the <a href="/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a> structure 
      passed in by the caller. VDS allocates memory for the <b>pwszName</b> member. Callers must 
      free the string by using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> 
      function.

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

<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_pack_prop">VDS_PACK_PROP</a>