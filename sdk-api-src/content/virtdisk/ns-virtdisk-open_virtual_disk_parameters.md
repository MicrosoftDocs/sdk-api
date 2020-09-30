---
UID: NS:virtdisk._OPEN_VIRTUAL_DISK_PARAMETERS
title: OPEN_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual disk open request parameters.
helpviewer_keywords: ["*POPEN_VIRTUAL_DISK_PARAMETERS","OPEN_VIRTUAL_DISK_PARAMETERS","OPEN_VIRTUAL_DISK_PARAMETERS structure [VHD]","OPEN_VIRTUAL_DISK_RW_DEPTH_DEFAULT","OPEN_VIRTUAL_DISK_VERSION_1","OPEN_VIRTUAL_DISK_VERSION_2","POPEN_VIRTUAL_DISK_PARAMETERS","POPEN_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_OPEN_VIRTUAL_DISK_PARAMETERS","vdssys/OPEN_VIRTUAL_DISK_PARAMETERS","vdssys/POPEN_VIRTUAL_DISK_PARAMETERS","vhd.open_virtual_disk_parameters","virtdisk/OPEN_VIRTUAL_DISK_PARAMETERS","virtdisk/POPEN_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\open_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: ad67bc3e-a0fe-4198-9307-819577abef7f
ms.date: 08/19/2020
ms.keywords: '*POPEN_VIRTUAL_DISK_PARAMETERS, OPEN_VIRTUAL_DISK_PARAMETERS, OPEN_VIRTUAL_DISK_PARAMETERS structure [VHD], OPEN_VIRTUAL_DISK_RW_DEPTH_DEFAULT, OPEN_VIRTUAL_DISK_VERSION_1, OPEN_VIRTUAL_DISK_VERSION_2, POPEN_VIRTUAL_DISK_PARAMETERS, POPEN_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _OPEN_VIRTUAL_DISK_PARAMETERS, vdssys/OPEN_VIRTUAL_DISK_PARAMETERS, vdssys/POPEN_VIRTUAL_DISK_PARAMETERS, vhd.open_virtual_disk_parameters, virtdisk/OPEN_VIRTUAL_DISK_PARAMETERS, virtdisk/POPEN_VIRTUAL_DISK_PARAMETERS'
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: OPEN_VIRTUAL_DISK_PARAMETERS, *POPEN_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPEN_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_OPEN_VIRTUAL_DISK_PARAMETERS
 - POPEN_VIRTUAL_DISK_PARAMETERS
 - virtdisk/POPEN_VIRTUAL_DISK_PARAMETERS
 - OPEN_VIRTUAL_DISK_PARAMETERS
 - virtdisk/OPEN_VIRTUAL_DISK_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - OPEN_VIRTUAL_DISK_PARAMETERS
---

# OPEN_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual disk open request parameters.

## -struct-fields

### -field Version

An <a href="/windows/win32/api/virtdisk/ne-virtdisk-open_virtual_disk_version">OPEN_VIRTUAL_DISK_VERSION</a> enumeration 
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


> [!NOTE]
> The following parameters prefaced Version3 are intended for internal use.

## -syntax

```cpp
typedef struct _OPEN_VIRTUAL_DISK_PARAMETERS {
  OPEN_VIRTUAL_DISK_VERSION Version;
  union {
    struct {
      ULONG RWDepth;
    } Version1;
    struct {
      BOOL GetInfoOnly;
      BOOL ReadOnly;
      GUID ResiliencyGuid;
    } Version2;
  };
} OPEN_VIRTUAL_DISK_PARAMETERS, *POPEN_VIRTUAL_DISK_PARAMETERS;
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>