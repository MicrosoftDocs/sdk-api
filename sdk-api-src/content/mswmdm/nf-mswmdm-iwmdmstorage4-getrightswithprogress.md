---
UID: NF:mswmdm.IWMDMStorage4.GetRightsWithProgress
title: IWMDMStorage4::GetRightsWithProgress (mswmdm.h)
author: windows-sdk-content
description: The GetRightsWithProgress method retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.
old-location: wmdm\iwmdmstorage4_getrightswithprogress.htm
tech.root: WMDM
ms.assetid: 63df4448-75f0-4152-a308-15f6f10e8564
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRightsWithProgress, GetRightsWithProgress method [windows Media Device Manager], GetRightsWithProgress method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetRightsWithProgress method, IWMDMStorage4.GetRightsWithProgress, IWMDMStorage4::GetRightsWithProgress, IWMDMStorage4GetRightsWithProgress, mswmdm/IWMDMStorage4::GetRightsWithProgress, wmdm.iwmdmstorage4_getrightswithprogress
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
 - IWMDMStorage4.GetRightsWithProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMStorage4::GetRightsWithProgress


## -description



The <b>GetRightsWithProgress</b> method retrieves the rights information for the storage object, providing a callback mechanism for monitoring progress.




## -parameters




### -param pIProgressCallback [in]

Optional pointer to an <a href="https://msdn.microsoft.com/fc3a7031-ac1b-45cf-889b-2d40d50b347d">IWMDMProgress3</a> interface to be used by Windows Media Device Manager to report progress back to the application.


### -param ppRights [out]

Pointer to an array of <a href="https://msdn.microsoft.com/1be9167b-0d20-4a17-a42b-9696ada2b539">WMDMRIGHTS</a> structures that contain the storage object rights information. Memory for this array is allocated by Windows Media Device Manager. When the calling application has finished accessing this array, the memory must be freed by using <b>CoTaskMemFree</b>.


### -param pnRightsCount [out]

Pointer to the number of <b>WMDMRIGHTS</b> structures in the <i>ppRights</i> array.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



Object rights describe the usage permissions for digital media content. For example, the <b>WMDMRIGHTS</b> structure can contain information concerning how many times a file can be played and who can play it.

Retrieving rights from a licensed file can sometimes be a lengthy request; this function allows a rights request to be performed asynchronously.

The secure content provider can generate event notifications on the callback <i>pIProgressCallback</i> in addition to the progress notifications. Examples of such events include acquiring a secure clock, initializing DRM, and so on. These events are described in <a href="https://msdn.microsoft.com/33f1de9c-f2eb-4b83-89a1-404a8c50ee08">IWMDMProgress3::Progress3</a>.

This method is identical to <a href="https://msdn.microsoft.com/5b654d32-b72a-44cf-a8d9-63fc0ae76171">IWMDMStorage::GetRights</a>, except it returns progress, and does not provide a MAC for parameter verification.




## -see-also




<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>
 

 

