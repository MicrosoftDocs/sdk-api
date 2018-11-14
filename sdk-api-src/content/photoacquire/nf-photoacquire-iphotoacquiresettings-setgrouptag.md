---
UID: NF:photoacquire.IPhotoAcquireSettings.SetGroupTag
title: IPhotoAcquireSettings::SetGroupTag
author: windows-sdk-content
description: The SetGroupTag method sets the group tag for an acquisition session.
old-location: picacq\iphotoacquiresettings_setgrouptag.htm
tech.root: acquisition
ms.assetid: f3c8b7dc-5701-412a-a376-498c40017d8f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetGroupTag method, IPhotoAcquireSettings.SetGroupTag, IPhotoAcquireSettings::SetGroupTag, IPhotoAcquireSettingsSetGroupTag, SetGroupTag, SetGroupTag method [Picture Acquisition], SetGroupTag method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetGroupTag, picacq.iphotoacquiresettings_setgrouptag
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
 - IPhotoAcquireSettings.SetGroupTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- photoacquire.h
: 
- IPhotoAcquireSettings.SetGroupTag
: 
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



The group tag is stored as a keyword in each file's metadata. It is also used in the file name if the <code>$(GroupTag)</code> token is present in the format string passed to <a href="https://msdn.microsoft.com/28eaeee4-05eb-4d51-9e21-937481bc7703">SetOutputFileNameTemplate</a>.




## -see-also




<a href="https://msdn.microsoft.com/4e65c5b2-ea1c-4376-a4bb-afbad7efb5ed">GetGroupTag</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>
 

 

