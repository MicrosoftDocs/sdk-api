---
UID: NS:winioctl._SET_DISK_ATTRIBUTES
title: "_SET_DISK_ATTRIBUTES"
author: windows-sdk-content
description: Specifies the attributes to be set on a disk device.
old-location: fs\set_disk_attributes.htm
old-project: FileIO
ms.assetid: 2caa79aa-24f9-481d-bbe3-ecd3e49bf316
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PSET_DISK_ATTRIBUTES, DISK_ATTRIBUTE_OFFLINE, DISK_ATTRIBUTE_READ_ONLY, PSET_DISK_ATTRIBUTES, PSET_DISK_ATTRIBUTES structure pointer [Files], SET_DISK_ATTRIBUTES, SET_DISK_ATTRIBUTES structure [Files], _SET_DISK_ATTRIBUTES, fs.set_disk_attributes, winioctl/PSET_DISK_ATTRIBUTES, winioctl/SET_DISK_ATTRIBUTES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: SET_DISK_ATTRIBUTES, *PSET_DISK_ATTRIBUTES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	SET_DISK_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _SET_DISK_ATTRIBUTES structure


## -description


Specifies the attributes to be set on a disk device. Passed as the input buffer to the 
    <a href="https://msdn.microsoft.com/ba0e3666-8660-493c-b821-5997d577e7e2">IOCTL_DISK_SET_DISK_ATTRIBUTES</a> control 
    code.


## -struct-fields




### -field Version

Set to <code>sizeof(GET_DISK_ATTRIBUTES)</code>.


### -field Persist

If <b>TRUE</b>, these settings are persisted across reboots.


### -field Reserved1

 Reserved. Must be set to <b>FALSE</b> (0).


### -field Attributes

 Specifies attributes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_OFFLINE"></a><a id="disk_attribute_offline"></a><dl>
<dt><b>DISK_ATTRIBUTE_OFFLINE</b></dt>
<dt>0x0000000000000001</dt>
</dl>
</td>
<td width="60%">
The disk is offline.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_READ_ONLY"></a><a id="disk_attribute_read_only"></a><dl>
<dt><b>DISK_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x0000000000000002</dt>
</dl>
</td>
<td width="60%">
The disk is read-only.

</td>
</tr>
</table>
 


### -field AttributesMask

Indicates which attributes are being changed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_OFFLINE"></a><a id="disk_attribute_offline"></a><dl>
<dt><b>DISK_ATTRIBUTE_OFFLINE</b></dt>
<dt>0x0000000000000001</dt>
</dl>
</td>
<td width="60%">
The offline attribute is being changed.

</td>
</tr>
<tr>
<td width="40%"><a id="DISK_ATTRIBUTE_READ_ONLY"></a><a id="disk_attribute_read_only"></a><dl>
<dt><b>DISK_ATTRIBUTE_READ_ONLY</b></dt>
<dt>0x0000000000000002</dt>
</dl>
</td>
<td width="60%">
The read-only attribute is being changed.

</td>
</tr>
</table>
 


### -field Reserved2

Reserved. Must be set to 0.


## -see-also




<a href="https://msdn.microsoft.com/dd55c570-68b5-4dc5-9fd0-a6e3277c318b">Disk Management Structures</a>



<a href="https://msdn.microsoft.com/c6a0461d-cc23-4191-a0ff-c4279c1b097e">GET_DISK_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/ba0e3666-8660-493c-b821-5997d577e7e2">IOCTL_DISK_SET_DISK_ATTRIBUTES</a>
 

 

