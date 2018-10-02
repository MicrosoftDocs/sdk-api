---
UID: NF:mswmdm.IWMDMObjectInfo.GetPlayLength
title: IWMDMObjectInfo::GetPlayLength
author: windows-sdk-content
description: The GetPlayLength method retrieves the play length of the object in units appropriate to the format. This is the remaining length that the file can play, not its total length.
old-location: wmdm\iwmdmobjectinfo_getplaylength.htm
tech.root: WMDM
ms.assetid: 7f553513-0928-41b8-858f-c06ec57660d1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPlayLength, GetPlayLength method [windows Media Device Manager], GetPlayLength method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetPlayLength method, IWMDMObjectInfo.GetPlayLength, IWMDMObjectInfo::GetPlayLength, IWMDMObjectInfoGetPlayLength, mswmdm/IWMDMObjectInfo::GetPlayLength, wmdm.iwmdmobjectinfo_getplaylength
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
 - IWMDMObjectInfo.GetPlayLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The value of the play length retrieved is either the total length of the object minus the current play position (if the <a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">SetPlayLength</a> method has not been called), or the value set by <b>SetPlayLength</b> clipped to be no greater than the total play length of the object minus the current play position.

The play length information can change either when the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a> method.

For folders or file systems containing playable files, the value returned is in tracks or numbers of playable files in that folder or in the root of that file system.




## -see-also




<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>



<a href="https://msdn.microsoft.com/7dfa6443-4eb8-4a88-8af1-c082750e8d22">SetPlayLength</a>
 

 

