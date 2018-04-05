---
UID: NF:photoacquire.IPhotoAcquireSettings.SetFlags
title: IPhotoAcquireSettings::SetFlags method
author: windows-driver-content
description: The SetFlags method sets the photo acquire flags.
old-location: picacq\iphotoacquiresettings_setflags.htm
old-project: acquisition
ms.assetid: aebe06d8-c764-4d2d-9bd2-58fd9e3714bd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPhotoAcquireSettings, IPhotoAcquireSettings interface [Picture Acquisition], SetFlags method, IPhotoAcquireSettings::SetFlags, IPhotoAcquireSettingsSetFlags, SetFlags method [Picture Acquisition], SetFlags method [Picture Acquisition], IPhotoAcquireSettings interface, SetFlags,IPhotoAcquireSettings.SetFlags, photoacquire/IPhotoAcquireSettings::SetFlags, picacq.iphotoacquiresettings_setflags
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PhotoAcquireUID.lib
-	PhotoAcquireUID.dll
api_name:
-	IPhotoAcquireSettings.SetFlags
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPhotoAcquireSettings::SetFlags method


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546791">GetFlags</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>
 

 

