---
UID: NF:vds.IVdsVDisk.GetProperties
title: IVdsVDisk::GetProperties (vds.h)
author: windows-sdk-content
description: Returns disk property information for the volume where the virtual disk resides.
old-location: base\ivdsvdisk_getproperties.htm
tech.root: VDS
ms.assetid: 0ecfbd1f-2f67-4d79-b081-7df071b070a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProperties, GetProperties method, GetProperties method,IVdsVDisk interface, IVdsVDisk interface,GetProperties method, IVdsVDisk.GetProperties, IVdsVDisk::GetProperties, base.ivdsvdisk_getproperties, vds/IVdsVDisk::GetProperties
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsVDisk.GetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVdsVDisk::GetProperties


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Returns disk property information for the volume where the virtual disk resides.


## -parameters




### -param pDiskProperties [out]

Receives a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-_vds_vdisk_properties">VDS_VDISK_PROPERTIES</a> structure containing the disk property information.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-common-return-codes">VDS-specific return values</a>. It can also return converted <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>  using the <a href="https://docs.microsoft.com/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://docs.microsoft.com/windows/desktop/VDS/about-vds">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
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
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vds/nn-vds-ivdsvdisk">IVdsVDisk</a>
 

 

