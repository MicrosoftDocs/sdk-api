---
UID: NF:vds.IVdsServiceUninstallDisk.GetDiskIdFromLunInfo
title: IVdsServiceUninstallDisk::GetDiskIdFromLunInfo (vds.h)
author: windows-sdk-content
description: Retrieves the VDS object ID for the disk that corresponds to a specified LUN.
old-location: base\ivdsserviceuninstalldisk_getdiskidfromluninfo.htm
tech.root: VDS
ms.assetid: 0059bb30-2799-4a41-8a5c-bae3aa2bcfc4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDiskIdFromLunInfo, GetDiskIdFromLunInfo method, GetDiskIdFromLunInfo method,IVdsServiceUninstallDisk interface, IVdsServiceUninstallDisk interface,GetDiskIdFromLunInfo method, IVdsServiceUninstallDisk.GetDiskIdFromLunInfo, IVdsServiceUninstallDisk::GetDiskIdFromLunInfo, base.ivdsserviceuninstalldisk_getdiskidfromluninfo, vds/IVdsServiceUninstallDisk::GetDiskIdFromLunInfo
ms.topic: method
f1_keywords: 
 - "vds/IVdsServiceUninstallDisk.GetDiskIdFromLunInfo"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsServiceUninstallDisk.GetDiskIdFromLunInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsServiceUninstallDisk::GetDiskIdFromLunInfo


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Retrieves the VDS object ID for the disk that corresponds to a specified LUN.


## -parameters




### -param pLunInfo [in]

The address of a <a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_lun_information">VDS_LUN_INFORMATION</a> structure that has been initialized by a VDS hardware provider.


### -param pDiskId [out]

The address of a VDS object ID variable passed in by the caller. This variable receives the GUID for the disk that corresponds to the LUN.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

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
The disk's GUID was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_NO_DISK_PATHNAME</b></dt>
<dt>0x8004270FL</dt>
</dl>
</td>
<td width="60%">
The disk's path could not be retrieved. Some operations on the disk may fail.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042405L</dt>
</dl>
</td>
<td width="60%">
The disk was not found.

</td>
</tr>
</table>
 




## -remarks



VDS implements this method. This method is called by VDS applications that need to uninstall a disk whose LUN is accessed through a VDS hardware provider on another computer. This method enables the application to uninstall a disk on a computer that does not have access to a VDS hardware provider and is thus unable to make an implicit link from disk to LUN.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsserviceuninstalldisk">IVdsServiceUninstallDisk</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdslun/ns-vdslun-_vds_lun_information">VDS_LUN_INFORMATION</a>
 

 

