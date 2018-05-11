---
UID: NN:mfidl.IMFSensorProfile
title: IMFSensorProfile
author: windows-driver-content
description: Describes a media foundation sensor profile.
old-location: mf\imfsensorprofile.htm
old-project: medfound
ms.assetid: 58D9FE3F-0F42-4262-B1BE-336BFA2E4BC7
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMFSensorProfile, IMFSensorProfile interface [Media Foundation], IMFSensorProfile interface [Media Foundation],described, mf.imfsensorprofile, mfidl/IMFSensorProfile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mfsensorgroup.dll
api_name:
-	IMFSensorProfile
product: Windows
targetos: Windows
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorProfile interface


## -description


Describes a media foundation sensor profile.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1D1EAD84-5053-47B2-9366-EEBE8681970F">AddBlockedControl</a>
</td>
<td align="left" width="63%">
    Adds the specified blocked control .

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D79C83AA-A105-4320-80D8-F7A3753DF4C4">AddProfileFilter</a>
</td>
<td align="left" width="63%">
Adds a profile filter to the specified media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EBBDCC39-8FF9-421B-867D-0AD950C2DDF5">GetProfileId</a>
</td>
<td align="left" width="63%">
Retrieves the sensor profile ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9535AF14-A6DF-49E9-B264-734B96A3DC29">IsMediaTypeSupported</a>
</td>
<td align="left" width="63%">
Determines if a media stream supports the specified media type.

</td>
</tr>
</table> 

