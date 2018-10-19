---
UID: NN:mfidl.IMFSensorProfileCollection
title: IMFSensorProfileCollection
author: windows-sdk-content
description: Contains a collection of media foundation sensor profile objects.
old-location: mf\imfsensorprofilecollection.htm
tech.root: medfound
ms.assetid: 406EDC3F-39AD-41E0-A8AA-E4476C93F353
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFSensorProfileCollection, IMFSensorProfileCollection interface [Media Foundation], IMFSensorProfileCollection interface [Media Foundation],described, mf.imfsensorprofilecollection, mfidl/IMFSensorProfileCollection
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfileCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorProfileCollection interface


## -description


Contains a collection of media foundation sensor profile objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorProfileCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorProfileCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorProfileCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt845817(v=VS.85).aspx">AddProfile</a>
</td>
<td align="left" width="63%">
Adds the specified profile to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt845818(v=VS.85).aspx">FindProfile</a>
</td>
<td align="left" width="63%">
Finds a profile based on the specified profile ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt845819(v=VS.85).aspx">GetProfile</a>
</td>
<td align="left" width="63%">
Retrieves the specified profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt845820(v=VS.85).aspx">RemoveProfile</a>
</td>
<td align="left" width="63%">
removes the specified profile based on the specified profile ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt845821(v=VS.85).aspx">RemoveProfileByIndex</a>
</td>
<td align="left" width="63%">
        Removes a profile based on the specified index.

</td>
</tr>
</table> 

