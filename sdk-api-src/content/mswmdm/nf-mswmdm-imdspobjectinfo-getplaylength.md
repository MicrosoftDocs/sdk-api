---
UID: NF:mswmdm.IMDSPObjectInfo.GetPlayLength
title: IMDSPObjectInfo::GetPlayLength
author: windows-sdk-content
description: The GetPlayLength method retrieves the play length of the object in units pertinent to the object. This is the remaining length that the object can play, not its total length.
old-location: wmdm\imdspobjectinfo_getplaylength.htm
tech.root: WMDM
ms.assetid: d5f2188f-f813-4c42-9878-52836ec8ebdc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetPlayLength, GetPlayLength method [windows Media Device Manager], GetPlayLength method [windows Media Device Manager],IMDSPObjectInfo interface, IMDSPObjectInfo interface [windows Media Device Manager],GetPlayLength method, IMDSPObjectInfo.GetPlayLength, IMDSPObjectInfo::GetPlayLength, IMDSPObjectInfoGetPlayLength, mswmdm/IMDSPObjectInfo::GetPlayLength, wmdm.imdspobjectinfo_getplaylength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObjectInfo.GetPlayLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">IMDSPObjectInfo::SetPlayLength</a> method has not been called), or the value set by <b>IMDSPObjectInfo::SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

For playable files, the value returned is specified in milliseconds. The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/d5d860fb-c146-4bfc-90b1-cf1dfc81c5ba">IMDSPObjectInfo::SetPlayLength</a>
 

 

