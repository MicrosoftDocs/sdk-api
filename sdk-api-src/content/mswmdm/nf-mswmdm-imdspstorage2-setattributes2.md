---
UID: NF:mswmdm.IMDSPStorage2.SetAttributes2
title: IMDSPStorage2::SetAttributes2 (mswmdm.h)
author: windows-sdk-content
description: The SetAttributes2 method extends IMDSPStorage::SetAttributes by enabling you to set audio and video formats and extended attributes of a storage object.
old-location: wmdm\imdspstorage2_setattributes2.htm
tech.root: WMDM
ms.assetid: f9c3f7e4-88b1-4842-aaaa-e6c52e1c3116
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMDSPStorage2 interface [windows Media Device Manager],SetAttributes2 method, IMDSPStorage2.SetAttributes2, IMDSPStorage2::SetAttributes2, IMDSPStorage2SetAttributes2, SetAttributes2, SetAttributes2 method [windows Media Device Manager], SetAttributes2 method [windows Media Device Manager],IMDSPStorage2 interface, mswmdm/IMDSPStorage2::SetAttributes2, wmdm.imdspstorage2_setattributes2
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
 - IMDSPStorage2.SetAttributes2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMDSPStorage2::SetAttributes2


## -description



The <b>SetAttributes2</b> method extends <b>IMDSPStorage::SetAttributes</b> by enabling you to set audio and video formats and extended attributes of a storage object.




## -parameters




### -param dwAttributes [in]

<b>DWORD</b> containing the attributes to be set as defined in the <b>IWMDMStorage::SetAttributes</b> method


### -param dwAttributesEx [in]

<b>DWORD</b> containing the extended attributes. No extended attributes are currently defined.


### -param pAudioFormat [in]

Pointer to a <b>_WAVEFORMATEX</b> structure that contains audio format information about the object. This parameter is optional and is ignored if the file is not audio.


### -param pVideoFormat [in]

Pointer to a <b>_VIDEOINFOHEADER</b> structure that contains video format information about the object. This parameter is optional and is ignored if the file is not video.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -remarks



See Remarks for <a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a>.

This method is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/39afb282-7141-4eb5-93e9-a69bef495d80">IMDSPStorage2 Interface</a>



<a href="https://msdn.microsoft.com/2db30715-cd49-4e55-b0d0-73ac531f8661">IMDSPStorage2::GetAttributes2</a>



<a href="https://msdn.microsoft.com/e995b255-364f-4ea6-b7fd-4443e84432ef">IMDSPStorage::SetAttributes</a>



<a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a>
 

 

