---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _OPEN_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual disk open request parameters.


## -struct-fields




### -field Version

An <a href="https://msdn.microsoft.com/3f45324a-6e31-43d6-9fc9-65c85e6c3493">OPEN_VIRTUAL_DISK_VERSION</a> enumeration 
      that specifies the version of the 
      <b>OPEN_VIRTUAL_DISK_PARAMETERS</b> structure 
      being passed to or from the VHD functions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OPEN_VIRTUAL_DISK_VERSION_1"></a><a id="open_virtual_disk_version_1"></a><dl>
<dt><b>OPEN_VIRTUAL_DISK_VERSION_1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the <b>Version1</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_VIRTUAL_DISK_VERSION_2"></a><a id="open_virtual_disk_version_2"></a><dl>
<dt><b>OPEN_VIRTUAL_DISK_VERSION_2</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use the <b>Version2</b> member of this structure.

</td>
</tr>
</table>
 


### -field Version1

This structure is used if the <b>Version</b> member is 
       <b>OPEN_VIRTUAL_DISK_VERSION_1</b> (1).


### -field Version1.RWDepth

Indicates the number of stores, beginning with the child, of the backing store chain to open as 
        read/write.  The remaining stores in the differencing chain will be opened read-only.  This is necessary for 
        merge operations to succeed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not open for read/write at any depth. This value should be used for read-only operations.

</td>
</tr>
<tr>
<td width="40%"><a id="OPEN_VIRTUAL_DISK_RW_DEPTH_DEFAULT"></a><a id="open_virtual_disk_rw_depth_default"></a><dl>
<dt><b>OPEN_VIRTUAL_DISK_RW_DEPTH_DEFAULT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Default value to use if no other value is desired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>n (user-defined)</dt>
</dl>
</td>
<td width="60%">
This integer value should be the number of merge levels plus one, if a merge operation is 
          intended.

</td>
</tr>
</table>
 


### -field Version2

This structure is used if the <b>Version</b> member is 
        <b>OPEN_VIRTUAL_DISK_VERSION_2</b> (2).

<b>Windows 7 and Windows Server 2008 R2:  </b>This structure is not supported until Windows 8 and Windows Server 2012.


### -field Version2.GetInfoOnly

If <b>TRUE</b>, indicates the handle is only to be used to get information on the virtual disk.


### -field Version2.ReadOnly

If <b>TRUE</b>, indicates the file backing store is to be opened as read-only.


### -field Version2.ResiliencyGuid

Resiliency <b>GUID</b> to specify when opening files.


### -field Version3

 


### -field Version3.GetInfoOnly

 


### -field Version3.ReadOnly

 


### -field Version3.ResiliencyGuid

 


### -field Version3.SnapshotId

 




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

