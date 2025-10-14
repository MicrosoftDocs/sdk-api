---
UID: NF:vds.IVdsHbaPort.GetProperties
title: IVdsHbaPort::GetProperties (vds.h)
description: Retrieves the properties of an HBA port.
helpviewer_keywords: ["GetProperties","GetProperties method [VDS]","GetProperties method [VDS]","IVdsHbaPort interface","IVdsHbaPort interface [VDS]","GetProperties method","IVdsHbaPort.GetProperties","IVdsHbaPort::GetProperties","base.ivdshbaport_getproperties","vds/IVdsHbaPort::GetProperties"]
old-location: base\ivdshbaport_getproperties.htm
tech.root: base
ms.assetid: 5472534f-66c8-4a78-a351-92f59e50ae32
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method [VDS], GetProperties method [VDS],IVdsHbaPort interface, IVdsHbaPort interface [VDS],GetProperties method, IVdsHbaPort.GetProperties, IVdsHbaPort::GetProperties, base.ivdshbaport_getproperties, vds/IVdsHbaPort::GetProperties
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - IVdsHbaPort::GetProperties
 - vds/IVdsHbaPort::GetProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vds.h
api_name:
 - IVdsHbaPort.GetProperties
---

# IVdsHbaPort::GetProperties


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the properties of an HBA port.

## -parameters

### -param pHbaPortProp [out]

The address of a member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a> structure 
      that is allocated and passed in by the caller.

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
The properties were successfully returned.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pHbaPortProp</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdshbaport">IVdsHbaPort</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>