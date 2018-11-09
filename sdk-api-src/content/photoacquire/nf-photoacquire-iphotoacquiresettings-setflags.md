---
UID: NF:photoacquire.IPhotoAcquireSettings.SetFlags
title: IPhotoAcquireSettings::SetFlags
author: windows-sdk-content
description: The SetFlags method sets the photo acquire flags.
old-location: picacq\iphotoacquiresettings_setflags.htm
tech.root: acquisition
ms.assetid: aebe06d8-c764-4d2d-9bd2-58fd9e3714bd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetFlags method, IPhotoAcquireSettings.SetFlags, IPhotoAcquireSettings::SetFlags, IPhotoAcquireSettingsSetFlags, SetFlags, SetFlags method [Picture Acquisition], SetFlags method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetFlags, picacq.iphotoacquiresettings_setflags
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
 - IPhotoAcquireSettings.SetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings::SetFlags


## -description



The <code>SetFlags</code> method sets the photo acquire flags.




## -parameters




### -param dwPhotoAcquireFlags [in]

Double word value containing the photo acquire flags.


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
 




## -see-also




<a href="https://msdn.microsoft.com/9ed9183b-c1a2-4251-bb65-bd947c2034ad">GetFlags</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>
 

 

