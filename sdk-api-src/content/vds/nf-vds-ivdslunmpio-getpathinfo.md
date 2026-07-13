---
UID: NF:vds.IVdsLunMpio.GetPathInfo
title: IVdsLunMpio::GetPathInfo (vds.h)
description: The IVdsLunMpio::GetPathInfo method (vds.h) returns an array of VDS_PATH_INFO structures, one for each path to the LUN.
helpviewer_keywords: ["GetPathInfo","GetPathInfo method [VDS]","GetPathInfo method [VDS]","IVdsLunMpio interface","IVdsLunMpio interface [VDS]","GetPathInfo method","IVdsLunMpio.GetPathInfo","IVdsLunMpio::GetPathInfo","base.ivdslunmpio_getpathinfo","vds/IVdsLunMpio::GetPathInfo","vdshwprv/IVdsLunMpio::GetPathInfo"]
old-location: base\ivdslunmpio_getpathinfo.htm
tech.root: base
ms.assetid: c7cc1abf-c7f2-4260-b9d2-f70128276e1e
ms.date: 08/05/2022
ms.keywords: GetPathInfo, GetPathInfo method [VDS], GetPathInfo method [VDS],IVdsLunMpio interface, IVdsLunMpio interface [VDS],GetPathInfo method, IVdsLunMpio.GetPathInfo, IVdsLunMpio::GetPathInfo, base.ivdslunmpio_getpathinfo, vds/IVdsLunMpio::GetPathInfo, vdshwprv/IVdsLunMpio::GetPathInfo
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
req.lib: Uuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - IVdsLunMpio::GetPathInfo
 - vds/IVdsLunMpio::GetPathInfo
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
 - IVdsLunMpio.GetPathInfo
---

# IVdsLunMpio::GetPathInfo


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns an array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a> structures, 
     one for each path to the LUN.

## -parameters

### -param ppPaths [out]

The address of a variable that receives an array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a> structures. Callers must free each element in the array, and the array itself, by using 
      the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

### -param plNumberOfPaths [out]

The address of a variable that receives the number of elements in the array returned in the 
      <i>ppPaths</i> parameter.
      

The number of paths returned by this method will match the number of paths returned by the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdslunmpio-getloadbalancepolicy">IVdsLunMpio::GetLoadBalancePolicy</a> 
       method.

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
The path information was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_PROVIDER_CACHE_CORRUPT</b></dt>
<dt>0x8004241FL</dt>
</dl>
</td>
<td width="60%">
The cache of the provider is corrupted. This indicates a software or communication problem inside a 
        provider that caches information about the attached devices. The caller can use the 
        <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-reenumerate">IVdsHwProvider::Reenumerate</a> method 
        followed by the  <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwprovider-refresh">IVdsHwProvider::Refresh</a> 
        method to restore the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_DELETED</b></dt>
<dt>0x8004240BL</dt>
</dl>
</td>
<td width="60%">
The LUN object is no longer present.

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
The LUN is in a failed state and is unable to perform the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ANOTHER_CALL_IN_PROGRESS</b></dt>
<dt>0x80042404L</dt>
</dl>
</td>
<td width="60%">
Another operation is in progress. This operation cannot proceed until previous operations are 
        complete.

</td>
</tr>
</table>

## -remarks

Hardware providers do not need to return the <b>VDS_OBJECT_ID</b> at hbaPortProp.id of 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a> and should just set this to 
    <b>GUID_NULL</b>. This ID will be filled in by the system when this call is passed back to 
    applications. If the service cannot find the corresponding HBA port,  <b>GUID_NULL</b> will be 
    used. The application will interpret this to mean that the HBA port is unknown to VDS.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nn-vdshwprv-ivdslunmpio">IVdsLunMpio</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a>
