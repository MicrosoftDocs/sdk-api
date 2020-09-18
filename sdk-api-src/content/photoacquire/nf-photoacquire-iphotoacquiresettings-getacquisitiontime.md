---
UID: NF:photoacquire.IPhotoAcquireSettings.GetAcquisitionTime
title: IPhotoAcquireSettings::GetAcquisitionTime (photoacquire.h)
description: The GetAcquisitionTime method retrieves the acquisition time of the current session.
helpviewer_keywords: ["GetAcquisitionTime","GetAcquisitionTime method [Picture Acquisition]","GetAcquisitionTime method [Picture Acquisition]","IPhotoAcquireSettings interface","IPhotoAcquireSettings interface [Picture Acquisition]","GetAcquisitionTime method","IPhotoAcquireSettings.GetAcquisitionTime","IPhotoAcquireSettings::GetAcquisitionTime","IPhotoAcquireSettingsGetAcquisitionTime","photoacquire/IPhotoAcquireSettings::GetAcquisitionTime","picacq.iphotoacquiresettings_getacquisitiontime"]
old-location: picacq\iphotoacquiresettings_getacquisitiontime.htm
tech.root: picacq
ms.assetid: 0acafc4d-e4f5-4dce-a192-18d27024ad83
ms.date: 12/05/2018
ms.keywords: GetAcquisitionTime, GetAcquisitionTime method [Picture Acquisition], GetAcquisitionTime method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetAcquisitionTime method, IPhotoAcquireSettings.GetAcquisitionTime, IPhotoAcquireSettings::GetAcquisitionTime, IPhotoAcquireSettingsGetAcquisitionTime, photoacquire/IPhotoAcquireSettings::GetAcquisitionTime, picacq.iphotoacquiresettings_getacquisitiontime
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
 - IPhotoAcquireSettings::GetAcquisitionTime
 - photoacquire/IPhotoAcquireSettings::GetAcquisitionTime
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
 - IPhotoAcquireSettings.GetAcquisitionTime
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

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setacquisitiontime">SetAcquisitionTime</a>