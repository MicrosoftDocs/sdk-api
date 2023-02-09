---
UID: NF:vds.IVdsVolumeMF.QueryAccessPaths
title: IVdsVolumeMF::QueryAccessPaths (vds.h)
description: Returns a list of access paths and a drive letter, if one exists, for the current volume.
helpviewer_keywords: ["IVdsVolumeMF interface [VDS]","QueryAccessPaths method","IVdsVolumeMF.QueryAccessPaths","IVdsVolumeMF::QueryAccessPaths","QueryAccessPaths","QueryAccessPaths method [VDS]","QueryAccessPaths method [VDS]","IVdsVolumeMF interface","base.ivdsvolumemf_queryaccesspaths","vds/IVdsVolumeMF::QueryAccessPaths"]
old-location: base\ivdsvolumemf_queryaccesspaths.htm
tech.root: base
ms.assetid: 7d541245-c189-4abe-ac72-2928c7aeed95
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF interface [VDS],QueryAccessPaths method, IVdsVolumeMF.QueryAccessPaths, IVdsVolumeMF::QueryAccessPaths, QueryAccessPaths, QueryAccessPaths method [VDS], QueryAccessPaths method [VDS],IVdsVolumeMF interface, base.ivdsvolumemf_queryaccesspaths, vds/IVdsVolumeMF::QueryAccessPaths
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
 - IVdsVolumeMF::QueryAccessPaths
 - vds/IVdsVolumeMF::QueryAccessPaths
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
 - IVdsVolumeMF.QueryAccessPaths
---

# IVdsVolumeMF::QueryAccessPaths


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a list of access paths and a drive letter, if one exists, for the current volume.

## -parameters

### -param pwszPathArray [out]

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>

### -param plNumberOfAccessPaths [out]

A pointer to the number of access paths on the volume.

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
<dt><b>VDS_E_OBJECT_STATUS_FAILED</b></dt>
<dt>0x80042431L</dt>
</dl>
</td>
<td width="60%">
The volume failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PACK_OFFLINE</b></dt>
<dt>0x80042444L</dt>
</dl>
</td>
<td width="60%">
The pack containing the volume is  not accessible.

</td>
</tr>
</table>

## -remarks

The drive letter appears as the first access path in <i>pwszPathArray</i>.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf">IVdsVolumeMF</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-addaccesspath">IVdsVolumeMF::AddAccessPath</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-deleteaccesspath">IVdsVolumeMF::DeleteAccessPath</a>