---
UID: NF:imapi2.IDiscRecorder2.get_DeviceCanLoadMedia
title: IDiscRecorder2::get_DeviceCanLoadMedia (imapi2.h)
author: windows-sdk-content
description: Determines if the device can eject and subsequently reload media.
old-location: imapi\idiscrecorder2_get_devicecanloadmedia.htm
tech.root: imapi
ms.assetid: aa6790aa-2999-4895-83fa-3967cb411741
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscRecorder2 interface [IMAPI],get_DeviceCanLoadMedia method, IDiscRecorder2.get_DeviceCanLoadMedia, IDiscRecorder2::get_DeviceCanLoadMedia, get_DeviceCanLoadMedia, get_DeviceCanLoadMedia method [IMAPI], get_DeviceCanLoadMedia method [IMAPI],IDiscRecorder2 interface, imapi.idiscrecorder2_get_devicecanloadmedia, imapi2/IDiscRecorder2::get_DeviceCanLoadMedia
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
 - IDiscRecorder2.get_DeviceCanLoadMedia
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscRecorder2::get_DeviceCanLoadMedia


## -description


Determines if the device can eject and subsequently reload media.


## -parameters




### -param value [out]

Is VARIANT_TRUE if the device can eject and subsequently reload media. If VARIANT_FALSE, loading media must be done manually.

<div class="alert"><b>Note</b>  For slim drives or laptop drives, which utilize a manual tray-loading mechanism, this parameter can indicate an  incorrect value of VARIANT_TRUE.</div>
<div> </div>

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



<a href="https://msdn.microsoft.com/d8fc55d7-0840-4090-a653-eb38d3f37fac">IDiscRecorder2::EjectMedia</a>
 

 

