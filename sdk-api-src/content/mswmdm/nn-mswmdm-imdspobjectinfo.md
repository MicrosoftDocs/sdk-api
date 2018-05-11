---
UID: NN:mswmdm.IMDSPObjectInfo
title: IMDSPObjectInfo
author: windows-driver-content
description: The IMDSPObjectInfo interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the IMDSPDeviceControl interface.
old-location: wmdm\imdspobjectinfo.htm
old-project: WMDM
ms.assetid: f0003b14-7ae7-4822-befe-6bb1779328ec
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMDSPObjectInfo, IMDSPObjectInfo interface [windows Media Device Manager], IMDSPObjectInfo interface [windows Media Device Manager],described, IMDSPObjectInfoInterface, mswmdm/IMDSPObjectInfo, wmdm.imdspobjectinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IMDSPObjectInfo
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPObjectInfo interface


## -description



The <b>IMDSPObjectInfo</b> interface provides methods for getting and setting parameters that describe how playable objects on a storage medium are referenced or accessed by the <a href="https://msdn.microsoft.com/a196edef-f670-4c1f-92bd-172a75f3f420">IMDSPDeviceControl</a> interface. Implementing this interface is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.

The resolution of the method parameters depends on the associated storage object as follows:

<ul>
<li>If the storage object represents a playable audio file, then the relative storage units are milliseconds.</li>
<li>If the storage object represents a folder or the root of a storage medium containing playable files, then the relative storage units are tracks.</li>
</ul>
This interface is not intended for non-playable files. If the <b>IMDSPObjectInfo</b> interface is acquired from an <a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> interface that represents a non-playable file or a folder or a root file system containing no playable files, E_INVALIDTYPE is returned from all of the methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPObjectInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPObjectInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPObjectInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ebd73b2-d168-470b-bc5a-aad8888c401a">GetLastPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the last play position of the object. The object must be a music file on the media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f83ff62c-63e3-4b15-9c5f-0ef39eaa3e0c">GetLongestPlayPosition</a>
</td>
<td align="left" width="63%">
Retrieves the longest play position of the object. The object must be a music file on the media device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5f2188f-f813-4c42-9878-52836ec8ebdc">GetPlayLength</a>
</td>
<td align="left" width="63%">
Retrieves the play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e801b95-aa44-4275-8a21-f68fbf6240f1">GetPlayOffset</a>
</td>
<td align="left" width="63%">
Retrieves the play offset of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abd18861-550b-4968-ac96-05f07315d4db">GetTotalLength</a>
</td>
<td align="left" width="63%">
Retrieves the total play length of the object in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">SetPlayLength</a>
</td>
<td align="left" width="63%">
Sets the play length of the object, in units pertinent to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f61ce3b5-3cd9-41e6-9a29-42b9832ec55a">SetPlayOffset</a>
</td>
<td align="left" width="63%">
Sets the play offset of the object, in units pertinent to the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

