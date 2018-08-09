---
UID: NF:photoacquire.IPhotoAcquireSettings.GetGroupTag
title: IPhotoAcquireSettings::GetGroupTag
author: windows-sdk-content
description: The GetGroupTag method retrieves a tag string for the group of files being downloaded from the device.
old-location: picacq\iphotoacquiresettings_getgrouptag.htm
old-project: acquisition
ms.assetid: 4e65c5b2-ea1c-4376-a4bb-afbad7efb5ed
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetGroupTag, GetGroupTag method [Picture Acquisition], GetGroupTag method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetGroupTag method, IPhotoAcquireSettings.GetGroupTag, IPhotoAcquireSettings::GetGroupTag, IPhotoAcquireSettingsGetGroupTag, photoacquire/IPhotoAcquireSettings::GetGroupTag, picacq.iphotoacquiresettings_getgrouptag
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
 - IPhotoAcquireSettings.GetGroupTag
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: ADAM
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



The group tag is stored as a keyword in each file's metadata. It is also used in the file name if the <code>$(GroupTag)</code> token is present in the format string passed to <a href="https://msdn.microsoft.com/ca36e3f9-74ad-4704-adeb-d3102668da30">SetOutputFileNameTemplate</a>.




## -see-also




<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/f3c8b7dc-5701-412a-a376-498c40017d8f">SetGroupTag</a>
 

 

