---
UID: NF:vds.IVdsVolumeMF3.FormatEx2
title: IVdsVolumeMF3::FormatEx2
author: windows-sdk-content
description: Formats a file system volume on a partition. This method is identical to the IVdsVolumeMF2::FormatEx method, except that formatting options are specified by using the Options parameter.
old-location: base\ivdsvolumemf3_formatex2.htm
tech.root: VDS
ms.assetid: b9ef47e2-552c-4630-9f63-84f00bd93fa6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FormatEx2, FormatEx2 method, FormatEx2 method,IVdsVolumeMF3 interface, IVdsVolumeMF3 interface,FormatEx2 method, IVdsVolumeMF3.FormatEx2, IVdsVolumeMF3::FormatEx2, base.ivdsvolumemf3_formatex2, vds/IVdsVolumeMF3::FormatEx2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsVolumeMF3.FormatEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVolumeMF3::FormatEx2


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Formats a file system volume on a partition. This method is identical to the <a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a> method, except that formatting options are specified by using the <i>Options</i> parameter.


## -parameters




### -param pwszFileSystemTypeName [in]

A <b>null</b>-terminated Unicode string containing the name of the file system with which to format the volume. This parameter can be <b>NULL</b> or the name of a Windows file system. The following file systems are supported: "NTFS", "FAT", "FAT32", "UDF", and "EXFAT". If this parameter is <b>NULL</b>, the default file system is used. For more information, see <a href="https://msdn.microsoft.com/78d60240-44dc-48b8-b2a6-5babbd79085f">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a>.


### -param usFileSystemRevision [in]

The revision of the file system, if any.  This member is expressed as a 16-bit binary-coded decimal number, where a decimal point is implied between the second and third digits. For example, a value of 0x0250 indicates revision 2.50.


### -param ulDesiredUnitAllocationSize [in]

The size of the allocation unit for the file system, in bytes.  The value must be a power of 2.  If the value is 0, a default allocation unit determined by the file system type will be used.  The allocation unit range is file system dependent.


### -param pwszLabel [in]

A <b>null</b>-terminated Unicode string to assign to the new file system.  The maximum label size is file system dependent.


### -param Options [in]

A bitmask of <a href="https://msdn.microsoft.com/75c92a9a-36c9-4c8d-90f2-a2b88cd8a7b5">VDS_FORMAT_OPTION_FLAGS</a> enumeration values that specify formatting options.


### -param ppAsync [out]

A pointer to an <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface that upon successful completion receives the <b>IVdsAsync</b> interface to monitor and control this operation.  Callers must release the interface received when they are done with it.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The file system was formatted successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_OPERATION_DENIED</b></dt>
<dt>0x8004240AL</dt>
</dl>
</td>
<td width="60%">
The operation is denied if the caller tries to format the system, boot, crashdump, hibernation, or pagefile volume.

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
The volume has failed.

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
The pack containing the volume is not accessible. All volumes in an offline pack are inaccessible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_FS_NOT_DETERMINED</b></dt>
<dt>0x80042593L</dt>
</dl>
</td>
<td width="60%">
The default file system could not be determined.

</td>
</tr>
</table>
 

In addition, the <a href="https://msdn.microsoft.com/7814b8ef-84b4-453e-b480-c32b67e5af93">IVdsAsync</a> interface can return the 
      following related warnings and error codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_FILE_SYSTEM</b></dt>
<dt>0x80042425L</dt>
</dl>
</td>
<td width="60%">
The file system is incompatible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INCOMPATIBLE_MEDIA</b></dt>
<dt>0x80042426L</dt>
</dl>
</td>
<td width="60%">
The media is incompatible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_ACCESS_DENIED</b></dt>
<dt>0x80042427L</dt>
</dl>
</td>
<td width="60%">
Access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_MEDIA_WRITE_PROTECTED</b></dt>
<dt>0x80042428L</dt>
</dl>
</td>
<td width="60%">
The media is write-protected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_BAD_LABEL</b></dt>
<dt>0x80042429L</dt>
</dl>
</td>
<td width="60%">
The label is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANT_QUICK_FORMAT</b></dt>
<dt>0x8004242AL</dt>
</dl>
</td>
<td width="60%">
The volume cannot be quick-formatted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_IO_ERROR</b></dt>
<dt>0x8004242BL</dt>
</dl>
</td>
<td width="60%">
An I/O error occurred during format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_TOO_SMALL</b></dt>
<dt>0x8004242CL</dt>
</dl>
</td>
<td width="60%">
The volume size is too small to format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_VOLUME_TOO_BIG</b></dt>
<dt>0x8004242DL</dt>
</dl>
</td>
<td width="60%">
The volume size is too large to format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_SIZE_TOO_SMALL</b></dt>
<dt>0x8004242EL</dt>
</dl>
</td>
<td width="60%">
The cluster size is too small to allow formatting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_SIZE_TOO_BIG</b></dt>
<dt>0x8004242FL</dt>
</dl>
</td>
<td width="60%">
The cluster size is too large to allow formatting.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CLUSTER_COUNT_BEYOND_32BITS</b></dt>
<dt>0x80042430L</dt>
</dl>
</td>
<td width="60%">
The number of clusters is too large to be represented as a 32-bit integer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_S_VOLUME_COMPRESS_FAILED</b></dt>
<dt>0x00042443L</dt>
</dl>
</td>
<td width="60%">
The file system is formatted but not compressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_CANT_INVALIDATE_FVE</b></dt>
<dt>0x80042592L</dt>
</dl>
</td>
<td width="60%">
BitLocker encryption could not be disabled for the volume.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c1d08018-4e9b-466a-b8dd-074b2ce0c8fe">IVdsVolumeMF2::FormatEx</a>



<a href="https://msdn.microsoft.com/46b8ff26-c00b-45ef-ac30-0aa82786bf9b">IVdsVolumeMF3</a>



<a href="https://msdn.microsoft.com/78d60240-44dc-48b8-b2a6-5babbd79085f">VDS_FILE_SYSTEM_FORMAT_SUPPORT_FLAG</a>



<a href="https://msdn.microsoft.com/75c92a9a-36c9-4c8d-90f2-a2b88cd8a7b5">VDS_FORMAT_OPTION_FLAGS</a>
 

 

