---
UID: NF:imapi2.IDiscRecorder2.get_VolumePathNames
title: IDiscRecorder2::get_VolumePathNames
author: windows-sdk-content
description: Retrieves a list of drive letters and NTFS mount points for the device.
old-location: imapi\idiscrecorder2_get_volumepathnames.htm
old-project: imapi
ms.assetid: 6e07553f-0d90-4b7d-95f8-0fe02c348695
ms.author: windowssdkdev
ms.date: 06/15/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_VolumePathNames method, IDiscRecorder2.get_VolumePathNames, IDiscRecorder2::get_VolumePathNames, get_VolumePathNames, get_VolumePathNames method [IMAPI], get_VolumePathNames method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_volumepathnames, imapi2/IDiscRecorder2::get_VolumePathNames
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IDiscRecorder2.get_VolumePathNames
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IDiscRecorder2::get_VolumePathNames


## -description


Retrieves a list of drive letters and NTFS mount points for the device.


## -parameters




### -param value [out]

List of drive letters and NTFS mount points for the device. Each element of the list is a <b>VARIANT</b> of type <b>VT_BSTR</b>. The <b>bstrVal</b> member of the variant contains the path.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/34f858b8-74eb-4725-8815-7954cb98cff0">IDiscRecorder2</a>



<a href="https://msdn.microsoft.com/14ec2007-3648-49b6-a96e-b682d592c2f1">IDiscRecorder2::get_LegacyDeviceNumber</a>
 

 

