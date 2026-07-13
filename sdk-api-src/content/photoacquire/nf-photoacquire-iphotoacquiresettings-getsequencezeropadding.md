---
UID: NF:photoacquire.IPhotoAcquireSettings.GetSequenceZeroPadding
title: IPhotoAcquireSettings::GetSequenceZeroPadding (photoacquire.h)
description: The GetSequenceZeroPadding method retrieves a value that indicates whether zeros or spaces will be used to pad sequential file names.
helpviewer_keywords: ["GetSequenceZeroPadding","GetSequenceZeroPadding method [Picture Acquisition]","GetSequenceZeroPadding method [Picture Acquisition]","IPhotoAcquireSettings interface","IPhotoAcquireSettings interface [Picture Acquisition]","GetSequenceZeroPadding method","IPhotoAcquireSettings.GetSequenceZeroPadding","IPhotoAcquireSettings::GetSequenceZeroPadding","IPhotoAcquireSettingsGetSequenceZeroPadding","photoacquire/IPhotoAcquireSettings::GetSequenceZeroPadding","picacq.iphotoacquiresettings_getsequencezeropadding"]
old-location: picacq\iphotoacquiresettings_getsequencezeropadding.htm
tech.root: picacq
ms.assetid: 72dc052a-bf8e-4876-8ab6-d0f6857941d5
ms.date: 12/05/2018
ms.keywords: GetSequenceZeroPadding, GetSequenceZeroPadding method [Picture Acquisition], GetSequenceZeroPadding method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetSequenceZeroPadding method, IPhotoAcquireSettings.GetSequenceZeroPadding, IPhotoAcquireSettings::GetSequenceZeroPadding, IPhotoAcquireSettingsGetSequenceZeroPadding, photoacquire/IPhotoAcquireSettings::GetSequenceZeroPadding, picacq.iphotoacquiresettings_getsequencezeropadding
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
 - IPhotoAcquireSettings::GetSequenceZeroPadding
 - photoacquire/IPhotoAcquireSettings::GetSequenceZeroPadding
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
 - IPhotoAcquireSettings.GetSequenceZeroPadding
---

# IPhotoAcquireSettings::GetSequenceZeroPadding


## -description

The <code>GetSequenceZeroPadding</code> method retrieves a value that indicates whether zeros or spaces will be used to pad sequential file names.

## -parameters

### -param pfZeroPad [out]

Pointer to a flag that, if set to <b>TRUE</b>, indicates that zeros will pad sequential file names.

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

A file name padded with zeros might appear as



``` syntax
"IMG0001.JPG"
```



The same file name without zero padding might appear as 



``` syntax
"IMG   1.JPG"
```


## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencezeropadding">SetSequenceZeroPadding</a>
