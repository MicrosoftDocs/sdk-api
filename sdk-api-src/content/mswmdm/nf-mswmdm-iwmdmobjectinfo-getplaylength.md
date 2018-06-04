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

# IWMDMObjectInfo::GetPlayLength


## -description



The <b>GetPlayLength</b> method retrieves the play length of the object in units appropriate to the format. This is the remaining length that the file can play, not its total length.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> specifying the remaining play length of the file, in milliseconds.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">SetPlayLength</a> method has not been called), or the value set by <b>SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.




## -see-also




<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>



<a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">SetPlayLength</a>
 

 

