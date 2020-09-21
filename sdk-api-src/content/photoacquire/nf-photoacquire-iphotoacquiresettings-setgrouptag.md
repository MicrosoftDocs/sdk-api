---
UID: NF:photoacquire.IPhotoAcquireSettings.SetGroupTag
title: IPhotoAcquireSettings::SetGroupTag (photoacquire.h)
description: The SetGroupTag method sets the group tag for an acquisition session.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","SetGroupTag method","IPhotoAcquireSettings.SetGroupTag","IPhotoAcquireSettings::SetGroupTag","IPhotoAcquireSettingsSetGroupTag","SetGroupTag","SetGroupTag method [Picture Acquisition]","SetGroupTag method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::SetGroupTag","picacq.iphotoacquiresettings_setgrouptag"]
old-location: picacq\iphotoacquiresettings_setgrouptag.htm
tech.root: picacq
ms.assetid: f3c8b7dc-5701-412a-a376-498c40017d8f
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetGroupTag method, IPhotoAcquireSettings.SetGroupTag, IPhotoAcquireSettings::SetGroupTag, IPhotoAcquireSettingsSetGroupTag, SetGroupTag, SetGroupTag method [Picture Acquisition], SetGroupTag method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetGroupTag, picacq.iphotoacquiresettings_setgrouptag
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
 - IPhotoAcquireSettings::SetGroupTag
 - photoacquire/IPhotoAcquireSettings::SetGroupTag
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
 - IPhotoAcquireSettings.SetGroupTag
---

# IPhotoAcquireSettings::SetGroupTag


## -description

The <code>SetGroupTag</code> method sets the group tag for an acquisition session.

## -parameters

### -param pszGroupTag [in]

Pointer to a null-terminated string containing the group tag.

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

The group tag is stored as a keyword in each file's metadata. It is also used in the file name if the <code>$(GroupTag)</code> token is present in the format string passed to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setoutputfilenametemplate">SetOutputFileNameTemplate</a>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getgrouptag">GetGroupTag</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>