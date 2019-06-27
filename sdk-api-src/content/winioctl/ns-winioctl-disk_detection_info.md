---
UID: NS:winioctl._DISK_DETECTION_INFO
title: DISK_DETECTION_INFO
author: windows-sdk-content
description: Contains detected drive parameters.
old-location: fs\disk_detection_info_str.htm
tech.root: FileIO
ms.assetid: 57ca68f4-f748-4bc4-90c3-13d545716d87
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDISK_DETECTION_INFO, DISK_DETECTION_INFO, DISK_DETECTION_INFO structure [Files], DetectExInt13, DetectInt13, DetectNone, PDISK_DETECTION_INFO, PDISK_DETECTION_INFO structure pointer [Files], _win32_disk_detection_info_str, base.disk_detection_info_str, fs.disk_detection_info_str, winioctl/DISK_DETECTION_INFO, winioctl/PDISK_DETECTION_INFO"
ms.topic: struct
f1_keywords: 
 - "winioctl/DISK_DETECTION_INFO"
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - DISK_DETECTION_INFO
product: Windows
targetos: Windows
req.typenames: DISK_DETECTION_INFO, *PDISK_DETECTION_INFO
req.redist: 
---

# DISK_DETECTION_INFO structure


## -description


Contains detected drive parameters.


## -struct-fields




### -field SizeOfDetectInfo

The size of the structure, in bytes.


### -field DetectionType

The detected partition type. 

This member can be one of the following values from the <b>DETECTION_TYPE</b> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DetectExInt13"></a><a id="detectexint13"></a><a id="DETECTEXINT13"></a><dl>
<dt><b>DetectExInt13</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The disk has an extended Int13 partition.

</td>
</tr>
<tr>
<td width="40%"><a id="DetectInt13"></a><a id="detectint13"></a><a id="DETECTINT13"></a><dl>
<dt><b>DetectInt13</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The disk has a standard Int13 partition.

</td>
</tr>
<tr>
<td width="40%"><a id="DetectNone"></a><a id="detectnone"></a><a id="DETECTNONE"></a><dl>
<dt><b>DetectNone</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The disk does not have an Int13 or an extended Int13 partition.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Int13

If <b>DetectionType</b> is DetectInt13, the union is a 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_int13_info">DISK_INT13_INFO</a> structure.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ExInt13

If <b>DetectionType</b> is DetectExInt13, the union is a 
<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_ex_int13_info">DISK_EX_INT13_INFO</a> structure.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_ex_int13_info">DISK_EX_INT13_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_geometry_ex">DISK_GEOMETRY_EX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winioctl/ns-winioctl-_disk_int13_info">DISK_INT13_INFO</a>
 

 

