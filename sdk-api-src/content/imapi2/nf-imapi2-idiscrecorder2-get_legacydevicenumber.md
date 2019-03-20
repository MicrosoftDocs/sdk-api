---
UID: NF:imapi2.IDiscRecorder2.get_LegacyDeviceNumber
title: IDiscRecorder2::get_LegacyDeviceNumber (imapi2.h)
author: windows-sdk-content
description: Retrieves the legacy device number for a CD or DVD device.
old-location: imapi\idiscrecorder2_get_legacydevicenumber.htm
tech.root: imapi
ms.assetid: 14ec2007-3648-49b6-a96e-b682d592c2f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_LegacyDeviceNumber method, IDiscRecorder2.get_LegacyDeviceNumber, IDiscRecorder2::get_LegacyDeviceNumber, get_LegacyDeviceNumber, get_LegacyDeviceNumber method [IMAPI], get_LegacyDeviceNumber method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_legacydevicenumber, imapi2/IDiscRecorder2::get_LegacyDeviceNumber
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2.get_LegacyDeviceNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder2::get_LegacyDeviceNumber


## -description


Retrieves  the legacy device number for a CD or DVD device.


## -parameters




### -param legacyDeviceNumber [out]

Zero-based index number of the device, based on the order the device was installed on the computer.

This value can change during PNP activity when devices are added or removed from the computer,  or across boot sessions and should not be considered a unique identifier for the device.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified failure.

Value: 0x80004005

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/6e07553f-0d90-4b7d-95f8-0fe02c348695">IDiscRecorder2::get_VolumePathNames</a>
 

 

