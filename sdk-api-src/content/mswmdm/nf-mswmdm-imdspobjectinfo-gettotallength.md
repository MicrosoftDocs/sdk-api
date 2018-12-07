---
UID: NF:mswmdm.IMDSPObjectInfo.GetTotalLength
title: IMDSPObjectInfo::GetTotalLength
author: windows-sdk-content
description: The GetTotalLength method retrieves the total play length of the object in units pertinent to the object. The value returned is the total length regardless of the current settings of the play length and offset.
old-location: wmdm\imdspobjectinfo_gettotallength.htm
tech.root: WMDM
ms.assetid: abd18861-550b-4968-ac96-05f07315d4db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTotalLength, GetTotalLength method [windows Media Device Manager], GetTotalLength method [windows Media Device Manager],IMDSPObjectInfo interface, IMDSPObjectInfo interface [windows Media Device Manager],GetTotalLength method, IMDSPObjectInfo.GetTotalLength, IMDSPObjectInfo::GetTotalLength, IMDSPObjectInfoGetTotalLength, mswmdm/IMDSPObjectInfo::GetTotalLength, wmdm.imdspobjectinfo_gettotallength
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
 - IMDSPObjectInfo.GetTotalLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPObjectInfo::GetTotalLength


## -description



The <b>GetTotalLength</b> method retrieves the total play length of the object in units pertinent to the object. The value returned is the total length regardless of the current settings of the play length and offset.




## -parameters




### -param pdwLength [out]

Pointer to a <b>DWORD</b> containing the total length of the object, in units pertinent to the object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



The value returned in the <i>pdwLength</i> parameter is the total length of the object regardless of the current settings of the play length and play offsets.

For playable files, the total length is specified in milliseconds.

For folders or file systems containing playable files, the value returned indicates the total number of playable files in a folder or in the root of a file system.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>
 

 

