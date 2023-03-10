---
UID: NF:vds.IVdsPack.Recover
title: IVdsPack::Recover (vds.h)
description: Returns a failing or failed pack to a healthy state, if possible. This method is supported only for dynamic packs.
helpviewer_keywords: ["IVdsPack interface [VDS]","Recover method","IVdsPack.Recover","IVdsPack::Recover","Recover","Recover method [VDS]","Recover method [VDS]","IVdsPack interface","base.ivdspack_recover","vds/IVdsPack::Recover"]
old-location: base\ivdspack_recover.htm
tech.root: base
ms.assetid: e558c2f4-e1a9-47c0-9b2f-972457e27bbf
ms.date: 12/05/2018
ms.keywords: IVdsPack interface [VDS],Recover method, IVdsPack.Recover, IVdsPack::Recover, Recover, Recover method [VDS], Recover method [VDS],IVdsPack interface, base.ivdspack_recover, vds/IVdsPack::Recover
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
 - IVdsPack::Recover
 - vds/IVdsPack::Recover
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
 - IVdsPack.Recover
---

# IVdsPack::Recover


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a failing or failed pack 
   to a healthy state, if possible. This method is supported only for dynamic packs.

## -parameters

### -param ppAsync [out]

The address of an <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> interface pointer, which VDS 
      initializes on return. Callers must release the interface. Use this interface to cancel, wait for, or query the 
      status of the operation.

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
The recovery completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_DMADMIN_METHOD_CALL_FAILED</b></dt>
<dt>0x80042420L</dt>
</dl>
</td>
<td width="60%">
The logical disk manager (LDM) service method failed.

</td>
</tr>
</table>

## -remarks

Although this method attempts to return a pack and all pack-related objects to a healthy state, it does not 
    always succeed. When successful, the <b>Recover</b> method 
    refreshes the state of all objects in the pack. It also synchronizes the providers with the underlying state of 
    the disks and other objects.
   

Implementers must return a pointer to the <a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a> 
    interface for this method, regardless of whether the call initiates an asynchronous operation.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdsasync">IVdsAsync</a>



<a href="/windows/desktop/api/vds/nn-vds-ivdspack">IVdsPack</a>