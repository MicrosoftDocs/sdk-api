---
UID: NF:photoacquire.IPhotoAcquireSettings.SetSequencePaddingWidth
title: IPhotoAcquireSettings::SetSequencePaddingWidth
author: windows-sdk-content
description: The SetSequencePaddingWidth method sets a value indicating how wide sequential fields in filenames will be.
old-location: picacq\iphotoacquiresettings_setsequencepaddingwidth.htm
tech.root: acquisition
ms.assetid: 2c90c109-1522-4722-a691-6f0f3caa50ec
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetSequencePaddingWidth method, IPhotoAcquireSettings.SetSequencePaddingWidth, IPhotoAcquireSettings::SetSequencePaddingWidth, IPhotoAcquireSettingsSetSequencePaddingWidth, SetSequencePaddingWidth, SetSequencePaddingWidth method [Picture Acquisition], SetSequencePaddingWidth method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetSequencePaddingWidth, picacq.iphotoacquiresettings_setsequencepaddingwidth
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPhotoAcquireSettings.SetSequencePaddingWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings::SetSequencePaddingWidth


## -description



The <code>SetSequencePaddingWidth</code> method sets a value indicating how wide sequential fields in filenames will be.




## -parameters




### -param dwWidth [in]

Double word value containing the width of sequential fields.


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



If the value passed to <code>SetSequencePaddingWidth</code> is nonzero and the format string specified in <a href="https://msdn.microsoft.com/28eaeee4-05eb-4d51-9e21-937481bc7703">SetOutputFileNameTemplate</a> contains a sequential token, this method sets the width allotted for the sequential token. For example, given the template <code>$(GroupTag)$(AcquisitionSequence).$(OriginalExtension)</code>, if padding is set to 0, a file name might appear as <pre class="syntax" xml:space="preserve"><code>"Image1.jpg"</code></pre> If padding is set to 3, the file name may appear as <pre class="syntax" xml:space="preserve"><code>"Image   1.jpg"</code></pre>





## -see-also




<a href="https://msdn.microsoft.com/d19a103e-0f5a-493d-a515-21d8730e39e3">GetSequencePaddingWidth</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/5010a61f-a01c-4dd9-850e-581a62b31ab4">SetSequenceZeroPadding</a>
 

 

