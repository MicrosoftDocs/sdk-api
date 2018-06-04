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

# _DISK_DETECTION_INFO structure


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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552624">DISK_INT13_INFO</a> structure.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ExInt13

If <b>DetectionType</b> is DetectExInt13, the union is a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff552610">DISK_EX_INT13_INFO</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552610">DISK_EX_INT13_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552618">DISK_GEOMETRY_EX</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552624">DISK_INT13_INFO</a>
 

 

