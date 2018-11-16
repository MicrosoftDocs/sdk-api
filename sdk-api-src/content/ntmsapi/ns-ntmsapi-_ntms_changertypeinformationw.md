---
UID: NS:ntmsapi._NTMS_CHANGERTYPEINFORMATIONW
title: "_NTMS_CHANGERTYPEINFORMATIONW"
author: windows-sdk-content
description: The NTMS_CHANGERTYPEINFORMATION structure defines the properties specific to a type of robotic changer supported by RSM.
old-location: fs\ntms_changertypeinformation.htm
tech.root: Rsm
ms.assetid: 49c219d7-5772-4868-80dd-ab1e1f1471b1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FILE_DEVICE_CHANGER, NTMS_CHANGERTYPEINFORMATION, NTMS_CHANGERTYPEINFORMATION structure [Files], NTMS_CHANGERTYPEINFORMATIONW, _NTMS_CHANGERTYPEINFORMATIONA, _NTMS_CHANGERTYPEINFORMATIONW, _zaw_ntms_changertypeinformation, base.ntms_changertypeinformation, fs.ntms_changertypeinformation, ntmsapi/NTMS_CHANGERTYPEINFORMATION
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntmsapi.h
req.include-header: 
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
 - Ntmsapi.h
api_name:
 - NTMS_CHANGERTYPEINFORMATION
product: Windows
targetos: Windows
req.typenames: NTMS_CHANGERTYPEINFORMATIONW
req.redist: 
---

# _NTMS_CHANGERTYPEINFORMATIONW structure


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>NTMS_CHANGERTYPEINFORMATION</b> structure defines the properties specific to a type of robotic changer supported by RSM.


## -struct-fields




### -field szVendor

Name of the vendor of the changer. This is acquired directly from the device inquiry data.


### -field szProduct

Product name of the changer. This is acquired directly from the device inquiry data.


### -field DeviceType

SCSI device type as reported from device inquiry data. From Winioctl.h. This can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_DEVICE_CHANGER"></a><a id="file_device_changer"></a><dl>
<dt><b>FILE_DEVICE_CHANGER</b></dt>
</dl>
</td>
<td width="60%">
Changer device.

</td>
</tr>
</table>
 


## -remarks



The 
<b>NTMS_CHANGERTYPEINFORMATION</b> structure is included in the 
<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/56e3380b-47c7-4861-bb2b-31d67ac10fe1">NTMS_OBJECTINFORMATION</a>
 

 

