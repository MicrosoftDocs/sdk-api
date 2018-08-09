---
UID: NF:mswmdm.IMDSPObjectInfo.GetLastPlayPosition
title: IMDSPObjectInfo::GetLastPlayPosition
author: windows-sdk-content
description: The GetLastPlayPosition method retrieves the last play position of the object. The object must be a music file on the media device.
old-location: wmdm\imdspobjectinfo_getlastplayposition.htm
old-project: WMDM
ms.assetid: 7ebd73b2-d168-470b-bc5a-aad8888c401a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetLastPlayPosition, GetLastPlayPosition method [windows Media Device Manager], GetLastPlayPosition method [windows Media Device Manager],IMDSPObjectInfo interface, IMDSPObjectInfo interface [windows Media Device Manager],GetLastPlayPosition method, IMDSPObjectInfo.GetLastPlayPosition, IMDSPObjectInfo::GetLastPlayPosition, IMDSPObjectInfoGetLastPlayPosition, mswmdm/IMDSPObjectInfo::GetLastPlayPosition, wmdm.imdspobjectinfo_getlastplayposition
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPObjectInfo.GetLastPlayPosition
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPObjectInfo::GetLastPlayPosition


## -description



The <b>GetLastPlayPosition</b> method retrieves the last play position of the object. The object must be a music file on the media device.




## -parameters




### -param pdwLastPos [out]

Pointer to a <b>DWORD</b> containing the last play position of the object, in milliseconds.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The object must be an audio data file. For all other object types, this function returns E_INVALIDTYPE.

The last play position changes when either the user starts playing a file on the media device or when an application invokes the <b>IMDSPDeviceControl::Play</b> method.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>
 

 

