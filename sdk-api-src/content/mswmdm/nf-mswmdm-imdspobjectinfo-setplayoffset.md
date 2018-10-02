---
UID: NF:mswmdm.IMDSPObjectInfo.SetPlayOffset
title: IMDSPObjectInfo::SetPlayOffset
author: windows-sdk-content
description: The SetPlayOffset method sets the play offset of the object, in the units pertinent to the object. This specifies the starting point for the next invocation of IMDSPDeviceControl::Play.
old-location: wmdm\imdspobjectinfo_setplayoffset.htm
tech.root: WMDM
ms.assetid: f61ce3b5-3cd9-41e6-9a29-42b9832ec55a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMDSPObjectInfo interface [windows Media Device Manager],SetPlayOffset method, IMDSPObjectInfo.SetPlayOffset, IMDSPObjectInfo::SetPlayOffset, IMDSPObjectInfoSetPlayOffset, SetPlayOffset, SetPlayOffset method [windows Media Device Manager], SetPlayOffset method [windows Media Device Manager],IMDSPObjectInfo interface, mswmdm/IMDSPObjectInfo::SetPlayOffset, wmdm.imdspobjectinfo_setplayoffset
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
 - IMDSPObjectInfo.SetPlayOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPObjectInfo::SetPlayOffset


## -description



The <b>SetPlayOffset</b> method sets the play offset of the object, in the units pertinent to the object. This specifies the starting point for the next invocation of <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">IMDSPDeviceControl::Play</a>.




## -parameters




### -param dwOffset [in]

<b>DWORD</b> containing the play offset to set for the object, in units pertinent to the object.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



If the value passed is greater than the total length of the object minus the current play length, it is clipped to the length of the object minus the play length.

For playable files, the value is specified in milliseconds. The play offset position value does not change when the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/09ca1922-3b33-47a8-a851-a1d221a568b9">IMDSPDeviceControl::Play</a> method.

For folders or file systems containing playable files, the value indicates the first track that is played when an application invokes the <b>IMDSPDeviceControl::Play</b> method.




## -see-also




<a href="https://msdn.microsoft.com/f0003b14-7ae7-4822-befe-6bb1779328ec">IMDSPObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/3e801b95-aa44-4275-8a21-f68fbf6240f1">IMDSPObjectInfo::GetPlayOffset</a>
 

 

