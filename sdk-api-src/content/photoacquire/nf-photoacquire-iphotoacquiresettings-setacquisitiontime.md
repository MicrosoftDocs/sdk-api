---
UID: NF:photoacquire.IPhotoAcquireSettings.SetAcquisitionTime
title: IPhotoAcquireSettings::SetAcquisitionTime
author: windows-sdk-content
description: The SetAcquisitionTime method sets the acquisition time explicitly.
old-location: picacq\iphotoacquiresettings_setacquisitiontime.htm
old-project: acquisition
ms.assetid: fc43be78-f35b-4159-a15c-c21cddee6c9e
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetAcquisitionTime method, IPhotoAcquireSettings.SetAcquisitionTime, IPhotoAcquireSettings::SetAcquisitionTime, IPhotoAcquireSettingsSetAcquisitionTime, SetAcquisitionTime, SetAcquisitionTime method [Picture Acquisition], SetAcquisitionTime method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetAcquisitionTime, picacq.iphotoacquiresettings_setacquisitiontime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSettings.SetAcquisitionTime
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPhotoAcquireSettings::SetAcquisitionTime


## -description



The <code>SetAcquisitionTime</code> method sets the acquisition time explicitly.




## -parameters




### -param pftAcquisitionTime [in]

Specifies the acquisition time.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method is typically used to force two sessions to show the same acquisition time. If not explicitly set, acquisition time defaults to the current machine time.




## -see-also




<a href="https://msdn.microsoft.com/0acafc4d-e4f5-4dce-a192-18d27024ad83">GetAcquisitionTime</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>
 

 

