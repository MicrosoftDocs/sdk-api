---
UID: NF:vds.IVdsSwProvider.CreatePack
title: IVdsSwProvider::CreatePack (vds.h)
description: Creates a pack object.
helpviewer_keywords: ["CreatePack","CreatePack method [VDS]","CreatePack method [VDS]","IVdsSwProvider interface","IVdsSwProvider interface [VDS]","CreatePack method","IVdsSwProvider.CreatePack","IVdsSwProvider::CreatePack","base.ivdsswprovider_createpack","vds/IVdsSwProvider::CreatePack"]
old-location: base\ivdsswprovider_createpack.htm
tech.root: base
ms.assetid: 2d711ed8-9101-4e68-b085-b5df01515b5d
ms.date: 12/05/2018
ms.keywords: CreatePack, CreatePack method [VDS], CreatePack method [VDS],IVdsSwProvider interface, IVdsSwProvider interface [VDS],CreatePack method, IVdsSwProvider.CreatePack, IVdsSwProvider::CreatePack, base.ivdsswprovider_createpack, vds/IVdsSwProvider::CreatePack
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
 - IVdsSwProvider::CreatePack
 - vds/IVdsSwProvider::CreatePack
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
 - IVdsSwProvider.CreatePack
---

# IVdsSwProvider::CreatePack


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Creates a pack object.

## -parameters

### -param ppPack [out]

The address of an <a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a> interface. Callers must release the interface.

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
<dt><b>VDS_E_ONLINE_PACK_EXISTS</b></dt>
<dt>0x80042464L</dt>
</dl>
</td>
<td width="60%">
Another dynamic pack exists with  <b>VDS_PS_ONLINE</b> status. Only one dynamic pack can have this status at a time.

</td>
</tr>
</table>

## -remarks

Use this method to create a pack before calling the <a href="/windows/desktop/api/vds/nf-vds-ivdspack-migratedisks">IVdsPack::MigrateDisks</a> method to convert disk formatting. When converting a basic disk to dynamic format,  pass either a new or existing pack as an argument to <b>MigrateDisks</b>. When converting a dynamic disk to basic format, use <b>CreatePack</b> to create a new, individual pack to hold the basic disk.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdspack-migratedisks">IVdsPack::MigrateDisks</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdsswprovider">IVdsSwProvider</a>