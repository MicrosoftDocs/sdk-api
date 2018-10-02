---
UID: NF:mswmdm.IWMDMObjectInfo.SetPlayOffset
title: IWMDMObjectInfo::SetPlayOffset
author: windows-sdk-content
description: The SetPlayOffset method sets the play offset of the object, in the units appropriate to the format. This specifies the starting point for the next invocation of Play.
old-location: wmdm\iwmdmobjectinfo_setplayoffset.htm
tech.root: WMDM
ms.assetid: b47cf5e8-1d5c-4a47-bb9a-0bec7203f497
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWMDMObjectInfo interface [windows Media Device Manager],SetPlayOffset method, IWMDMObjectInfo.SetPlayOffset, IWMDMObjectInfo::SetPlayOffset, IWMDMObjectInfoSetPlayOffset, SetPlayOffset, SetPlayOffset method [windows Media Device Manager], SetPlayOffset method [windows Media Device Manager],IWMDMObjectInfo interface, mswmdm/IWMDMObjectInfo::SetPlayOffset, wmdm.iwmdmobjectinfo_setplayoffset
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
 - IWMDMObjectInfo.SetPlayOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMObjectInfo::SetPlayOffset


## -description



The <b>SetPlayOffset</b> method sets the play offset of the object, in the units appropriate to the format. This specifies the starting point for the next invocation of <b>Play</b>.




## -parameters




### -param dwOffset [in]

<b>DWORD</b> specifying the play offset, in units appropriate to the format.


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

For playable files, the value is specified in milliseconds. The play offset position value does not change when the user starts playing a file on the media device or when an application invokes the <b>IWMDMDeviceControl::Play</b> method.

For folders or file systems containing playable files, the value indicates the first track that is played when an application invokes the <b>IWMDMDeviceControl::Play</b> method.




## -see-also




<a href="https://msdn.microsoft.com/8642404a-33ff-40b7-b05a-f193e8feadf5">GetPlayOffset</a>



<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>
 

 

