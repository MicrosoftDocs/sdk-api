---
UID: NF:photoacquire.IPhotoAcquireSettings.GetGroupTag
title: IPhotoAcquireSettings::GetGroupTag (photoacquire.h)
description: The GetGroupTag method retrieves a tag string for the group of files being downloaded from the device.
helpviewer_keywords: ["GetGroupTag","GetGroupTag method [Picture Acquisition]","GetGroupTag method [Picture Acquisition]","IPhotoAcquireSettings interface","IPhotoAcquireSettings interface [Picture Acquisition]","GetGroupTag method","IPhotoAcquireSettings.GetGroupTag","IPhotoAcquireSettings::GetGroupTag","IPhotoAcquireSettingsGetGroupTag","photoacquire/IPhotoAcquireSettings::GetGroupTag","picacq.iphotoacquiresettings_getgrouptag"]
old-location: picacq\iphotoacquiresettings_getgrouptag.htm
tech.root: picacq
ms.assetid: 4e65c5b2-ea1c-4376-a4bb-afbad7efb5ed
ms.date: 12/05/2018
ms.keywords: GetGroupTag, GetGroupTag method [Picture Acquisition], GetGroupTag method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetGroupTag method, IPhotoAcquireSettings.GetGroupTag, IPhotoAcquireSettings::GetGroupTag, IPhotoAcquireSettingsGetGroupTag, photoacquire/IPhotoAcquireSettings::GetGroupTag, picacq.iphotoacquiresettings_getgrouptag
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
 - IPhotoAcquireSettings::GetGroupTag
 - photoacquire/IPhotoAcquireSettings::GetGroupTag
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
 - IPhotoAcquireSettings.GetGroupTag
---

# IPhotoAcquireSettings::GetGroupTag


## -description

The <code>GetGroupTag</code> method retrieves a tag string for the group of files being downloaded from the device.

## -parameters

### -param pbstrGroupTag [out]

Pointer to a string containing the group tag.

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

The group tag is stored as a keyword in each file's metadata. It is also used in the file name if the <code>$(GroupTag)</code> token is present in the format string passed to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getoutputfilenametemplate">SetOutputFileNameTemplate</a>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setgrouptag">SetGroupTag</a>