---
UID: NF:photoacquire.IPhotoAcquireSettings.SetSequenceZeroPadding
title: IPhotoAcquireSettings::SetSequenceZeroPadding (photoacquire.h)
description: The SetSequenceZeroPadding method sets a value indicating whether zeros or spaces are used to pad sequential file names.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","SetSequenceZeroPadding method","IPhotoAcquireSettings.SetSequenceZeroPadding","IPhotoAcquireSettings::SetSequenceZeroPadding","IPhotoAcquireSettingsSetSequenceZeroPadding","SetSequenceZeroPadding","SetSequenceZeroPadding method [Picture Acquisition]","SetSequenceZeroPadding method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::SetSequenceZeroPadding","picacq.iphotoacquiresettings_setsequencezeropadding"]
old-location: picacq\iphotoacquiresettings_setsequencezeropadding.htm
tech.root: picacq
ms.assetid: 5010a61f-a01c-4dd9-850e-581a62b31ab4
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetSequenceZeroPadding method, IPhotoAcquireSettings.SetSequenceZeroPadding, IPhotoAcquireSettings::SetSequenceZeroPadding, IPhotoAcquireSettingsSetSequenceZeroPadding, SetSequenceZeroPadding, SetSequenceZeroPadding method [Picture Acquisition], SetSequenceZeroPadding method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetSequenceZeroPadding, picacq.iphotoacquiresettings_setsequencezeropadding
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
 - IPhotoAcquireSettings::SetSequenceZeroPadding
 - photoacquire/IPhotoAcquireSettings::SetSequenceZeroPadding
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
 - IPhotoAcquireSettings.SetSequenceZeroPadding
---

# IPhotoAcquireSettings::SetSequenceZeroPadding


## -description

The <code>SetSequenceZeroPadding</code> method sets a value indicating whether zeros or spaces are used to pad sequential file names.

## -parameters

### -param fZeroPad [in]

Flag that, if set to <b>TRUE</b>, indicates that zeros pad sequential file names.

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

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getsequencezeropadding">GetSequenceZeroPadding</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencepaddingwidth">SetSequencePaddingWidth</a>
