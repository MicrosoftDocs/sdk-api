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

# IMDSPObjectInfo::GetPlayOffset


## -description



The <b>GetPlayOffset</b> method retrieves the play offset of the object, in units pertinent to the object. This is the starting point for the next invocation of <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">IMDSPDeviceControl::Play</a>.




## -parameters




### -param pdwOffset [out]

Pointer to a <b>DWORD</b> containing the play offset of the object, in units pertinent to the object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The value retrieved is either zero (if the <a href="https://msdn.microsoft.com/f61ce3b5-3cd9-41e6-9a29-42b9832ec55a">SetPlayOffset</a> method has not been called) or the value set by <b>SetPlayOffset</b> clipped to be no greater than the total play length of the object minus one unit.

For playable files, the value returned is specified in milliseconds. The play offset value does not change when the user starts playing a file on the media device or when an application invokes the <b>IMDSPDeviceControl::Play</b> method.

For folders or file systems containing playable files, the value returned indicates the first track that is played when an application invokes the <b>IMDSPDeviceControl::Play</b> method.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/f61ce3b5-3cd9-41e6-9a29-42b9832ec55a">IMDSPObjectInfo::SetPlayOffset</a>
 

 

