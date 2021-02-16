---
UID: NF:photoacquire.IPhotoAcquireSettings.SetAcquisitionTime
title: IPhotoAcquireSettings::SetAcquisitionTime (photoacquire.h)
description: The SetAcquisitionTime method sets the acquisition time explicitly.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","SetAcquisitionTime method","IPhotoAcquireSettings.SetAcquisitionTime","IPhotoAcquireSettings::SetAcquisitionTime","IPhotoAcquireSettingsSetAcquisitionTime","SetAcquisitionTime","SetAcquisitionTime method [Picture Acquisition]","SetAcquisitionTime method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::SetAcquisitionTime","picacq.iphotoacquiresettings_setacquisitiontime"]
old-location: picacq\iphotoacquiresettings_setacquisitiontime.htm
tech.root: picacq
ms.assetid: fc43be78-f35b-4159-a15c-c21cddee6c9e
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetAcquisitionTime method, IPhotoAcquireSettings.SetAcquisitionTime, IPhotoAcquireSettings::SetAcquisitionTime, IPhotoAcquireSettingsSetAcquisitionTime, SetAcquisitionTime, SetAcquisitionTime method [Picture Acquisition], SetAcquisitionTime method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetAcquisitionTime, picacq.iphotoacquiresettings_setacquisitiontime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireSettings::SetAcquisitionTime
 - photoacquire/IPhotoAcquireSettings::SetAcquisitionTime
dev_langs:
 - c++
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

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getacquisitiontime">GetAcquisitionTime</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>