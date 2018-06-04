---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMDSPObjectInfo::GetPlayLength


## -description



The <b>GetPlayLength</b> method retrieves the play length of the object in units pertinent to the object. This is the remaining length that the object can play, not its total length.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the remaining play length of the object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">IMDSPObjectInfo::SetPlayLength</a> method has not been called), or the value set by <b>IMDSPObjectInfo::SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

For playable files, the value returned is specified in milliseconds. The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">IMDSPObjectInfo::SetPlayLength</a>
 

 

