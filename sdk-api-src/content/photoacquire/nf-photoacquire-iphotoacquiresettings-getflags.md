---
UID: NF:photoacquire.IPhotoAcquireSettings.GetFlags
title: IPhotoAcquireSettings::GetFlags (photoacquire.h)
author: windows-sdk-content
description: The GetFlags method retrieves the photo acquire flags.
old-location: picacq\iphotoacquiresettings_getflags.htm
tech.root: acquisition
ms.assetid: 9ed9183b-c1a2-4251-bb65-bd947c2034ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFlags, GetFlags method [Picture Acquisition], GetFlags method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetFlags method, IPhotoAcquireSettings.GetFlags, IPhotoAcquireSettings::GetFlags, IPhotoAcquireSettingsGetFlags, photoacquire/IPhotoAcquireSettings::GetFlags, picacq.iphotoacquiresettings_getflags
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
 - IPhotoAcquireSettings.GetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings::GetFlags


## -description



The <code>GetFlags</code> method retrieves the photo acquire flags.




## -parameters




### -param pdwPhotoAcquireFlags [out]

Pointer to a double word value containing the photo acquire flags.


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
 




## -see-also




<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>



<a href="https://msdn.microsoft.com/aebe06d8-c764-4d2d-9bd2-58fd9e3714bd">SetFlags</a>
 

 

