---
UID: NF:mswmdm.IWMDMObjectInfo.GetLastPlayPosition
title: IWMDMObjectInfo::GetLastPlayPosition
author: windows-sdk-content
description: The GetLastPlayPosition method retrieves the last play position of the object. The object must be an audio file on the media device.
old-location: wmdm\iwmdmobjectinfo_getlastplayposition.htm
old-project: WMDM
ms.assetid: d5b5cf7c-6969-497e-bf2c-e91ddb85f701
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetLastPlayPosition, GetLastPlayPosition method [windows Media Device Manager], GetLastPlayPosition method [windows Media Device Manager],IWMDMObjectInfo interface, IWMDMObjectInfo interface [windows Media Device Manager],GetLastPlayPosition method, IWMDMObjectInfo.GetLastPlayPosition, IWMDMObjectInfo::GetLastPlayPosition, IWMDMObjectInfoGetLastPlayPosition, mswmdm/IWMDMObjectInfo::GetLastPlayPosition, wmdm.iwmdmobjectinfo_getlastplayposition
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	IWMDMObjectInfo.GetLastPlayPosition
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMObjectInfo::GetLastPlayPosition


## -description



The <b>GetLastPlayPosition</b> method retrieves the last play position of the object. The object must be an audio file on the media device.




## -parameters




### -param pdwLastPos [out]

Pointer to a <b>DWORD</b> specifying the last play position of the object, in milliseconds.


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

The last play position changes when either the user starts playing a file on the media device or when an application invokes the <a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">IWMDMDeviceControl::Play</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ebc6ad10-02c1-4cc9-8a09-d1fe7aef146a">IWMDMObjectInfo Interface</a>



<a href="https://msdn.microsoft.com/e8d717e6-365c-44ad-b24e-daa3c35664de">Play</a>
 

 

