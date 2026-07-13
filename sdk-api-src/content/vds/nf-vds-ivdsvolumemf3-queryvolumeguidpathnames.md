---
UID: NF:vds.IVdsVolumeMF3.QueryVolumeGuidPathnames
title: IVdsVolumeMF3::QueryVolumeGuidPathnames (vds.h)
description: Returns a list of volume GUID paths for the current volume.
helpviewer_keywords: ["IVdsVolumeMF3 interface","QueryVolumeGuidPathnames method","IVdsVolumeMF3.QueryVolumeGuidPathnames","IVdsVolumeMF3::QueryVolumeGuidPathnames","QueryVolumeGuidPathnames","QueryVolumeGuidPathnames method","QueryVolumeGuidPathnames method","IVdsVolumeMF3 interface","base.ivdsvolumemf3_queryvolumeguidpathnames","vds/IVdsVolumeMF3::QueryVolumeGuidPathnames"]
old-location: base\ivdsvolumemf3_queryvolumeguidpathnames.htm
tech.root: base
ms.assetid: 08311403-23a9-4191-9720-3cec805de825
ms.date: 12/05/2018
ms.keywords: IVdsVolumeMF3 interface,QueryVolumeGuidPathnames method, IVdsVolumeMF3.QueryVolumeGuidPathnames, IVdsVolumeMF3::QueryVolumeGuidPathnames, QueryVolumeGuidPathnames, QueryVolumeGuidPathnames method, QueryVolumeGuidPathnames method,IVdsVolumeMF3 interface, base.ivdsvolumemf3_queryvolumeguidpathnames, vds/IVdsVolumeMF3::QueryVolumeGuidPathnames
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsVolumeMF3::QueryVolumeGuidPathnames
 - vds/IVdsVolumeMF3::QueryVolumeGuidPathnames
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
 - IVdsVolumeMF3.QueryVolumeGuidPathnames
---

# IVdsVolumeMF3::QueryVolumeGuidPathnames


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns a list of volume GUID paths for the current volume.

## -parameters

### -param pwszPathArray [out]

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>

### -param pulNumberOfPaths [out]

A pointer to a variable that receives the number of volume GUID paths returned in the buffer pointed to by the <i>pwszPathArray</i> parameter.

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
<dt><b>VDS_E_INTERNAL_ERROR</b></dt>
<dt>0x80042448L</dt>
</dl>
</td>
<td width="60%">
An internal error occurred. Check the event log for more details.

</td>
</tr>
</table>

## -remarks

A volume GUID path is a string of the form "\\?\Volume{GUID}\" where GUID is a GUID that identifies the volume.

## -see-also

<a href="/windows/desktop/api/vds/nn-vds-ivdsvolumemf3">IVdsVolumeMF3</a>