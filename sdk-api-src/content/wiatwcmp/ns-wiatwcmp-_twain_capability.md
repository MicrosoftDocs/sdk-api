---
UID: NS:wiatwcmp._TWAIN_CAPABILITY
title: "_TWAIN_CAPABILITY"
author: windows-driver-content
description: The TWAIN_CAPABILITY structure holds information used when a TWAIN-compatible application communicates with a WIA driver.
old-location: image\twain_capability.htm
old-project: image
ms.assetid: 79a2155d-eb06-4095-9fe6-b95d93e46211
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PTWAIN_CAPABILITY, PTWAIN_CAPABILITY, PTWAIN_CAPABILITY structure pointer [Imaging Devices], TWAIN_CAPABILITY, TWAIN_CAPABILITY structure [Imaging Devices], _TWAIN_CAPABILITY, image.twain_capability, wiastrct_12204cb8-d0ad-46d5-a741-4522ba28006b.xml, wiatwcmp/PTWAIN_CAPABILITY, wiatwcmp/TWAIN_CAPABILITY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiatwcmp.h
req.include-header: Wiatwcmp.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: TWAIN_CAPABILITY, *PTWAIN_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiatwcmp.h
api_name:
-	TWAIN_CAPABILITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _TWAIN_CAPABILITY structure


## -description


The TWAIN_CAPABILITY structure holds information used when a TWAIN-compatible application communicates with a WIA driver.


## -struct-fields




### -field lSize

Specifies the size, in bytes, of the TWAIN_CAPABILITY structure.


### -field lMSG

Specifies the particular TWAIN message, which can be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
MSG_GET

</td>
<td>
Get a capability.

</td>
</tr>
<tr>
<td>
MSG_GETCURRENT

</td>
<td>
Get the current capability.

</td>
</tr>
<tr>
<td>
MSG_GETDEFAULT

</td>
<td>
Get the default capability.

</td>
</tr>
<tr>
<td>
MSG_RESET

</td>
<td>
Reset the capability.

</td>
</tr>
<tr>
<td>
MSG_SET

</td>
<td>
Set a capability.

</td>
</tr>
</table>
 


### -field lCapID

Specifies the ID of the capability to set or get.


### -field lConType

Specifies the capability's container type.


### -field lRC

Specifies the TWAIN return code. This value can be on of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TWRC_FAILURE

</td>
<td>
The capability specified by the <b>lCapID</b> member is not supported.

</td>
</tr>
<tr>
<td>
TWRC_SUCCESS

</td>
<td>
The capability specified by the <b>lCapID</b> member is supported.

</td>
</tr>
<tr>
<td>
Other TWRC_XXX return code

</td>
<td>
See the <b>Remarks</b> section.

</td>
</tr>
</table>
 


### -field lCC

Specifies the TWAIN condition code. This value can be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
TWCC_BUMMER

</td>
<td>
The operation failed for an unknown reason.

</td>
</tr>
<tr>
<td>
TWCC_SUCCESS

</td>
<td>
The operation was successful.

</td>
</tr>
<tr>
<td>
TWCC_XXX

</td>
<td>
See the <b>Remarks</b> section.

</td>
</tr>
</table>
 


### -field lDataSize

Specifies the size, in bytes of the data in the <b>Data</b> array.


### -field Data

Is an array that contains the capability data. The actual size, in bytes, of the array is indicated by the <b>lDataSize</b> member.


## -remarks



A TWAIN-capable application communicates with a WIA driver by way of the TWAIN compatibility later to find out whether the driver has any private capabilities, and if so, what they are. A TWAIN_CAPABILITY structure is used in this communication. For more information, see <a href="https://msdn.microsoft.com/270e62dd-590c-4495-be22-002957932031">TWAIN Compatibility</a>. 

The TWAIN return codes and control codes are defined in <i>twain.h</i>, which can be obtained from the TWAIN Working Group (http://www.twain.org).



