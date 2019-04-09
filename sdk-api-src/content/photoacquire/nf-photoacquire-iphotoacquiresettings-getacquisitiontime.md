---
UID: NF:photoacquire.IPhotoAcquireSettings.GetAcquisitionTime
title: IPhotoAcquireSettings::GetAcquisitionTime (photoacquire.h)
author: windows-sdk-content
description: The GetAcquisitionTime method retrieves the acquisition time of the current session.
old-location: picacq\iphotoacquiresettings_getacquisitiontime.htm
tech.root: acquisition
ms.assetid: 0acafc4d-e4f5-4dce-a192-18d27024ad83
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAcquisitionTime, GetAcquisitionTime method [Picture Acquisition], GetAcquisitionTime method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetAcquisitionTime method, IPhotoAcquireSettings.GetAcquisitionTime, IPhotoAcquireSettings::GetAcquisitionTime, IPhotoAcquireSettingsGetAcquisitionTime, photoacquire/IPhotoAcquireSettings::GetAcquisitionTime, picacq.iphotoacquiresettings_getacquisitiontime
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSettings.GetAcquisitionTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings::GetAcquisitionTime


## -description



The <code>GetAcquisitionTime</code> method retrieves the acquisition time of the current session.




## -parameters




### -param pftAcquisitionTime [out]

Specifies acquisition time.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A non-NULL value was expected.

</td>
</tr>
</table>
 




## -remarks



If not set explicitly, the acquisition time defaults to the current machine time.




## -see-also




<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/fc43be78-f35b-4159-a15c-c21cddee6c9e">SetAcquisitionTime</a>
 

 

