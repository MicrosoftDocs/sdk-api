---
UID: NF:mswmdm.IWMDMStorage2.SetAttributes2
title: IWMDMStorage2::SetAttributes2
author: windows-sdk-content
description: The SetAttributes2 method sets extended attributes of the storage.
old-location: wmdm\iwmdmstorage2_setattributes2.htm
old-project: WMDM
ms.assetid: 0a2e143e-8d6a-497e-9c45-fd3349c4ec97
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWMDMStorage2 interface [windows Media Device Manager],SetAttributes2 method, IWMDMStorage2.SetAttributes2, IWMDMStorage2::SetAttributes2, IWMDMStorage2SetAttributes2, SetAttributes2, SetAttributes2 method [windows Media Device Manager], SetAttributes2 method [windows Media Device Manager],IWMDMStorage2 interface, mswmdm/IWMDMStorage2::SetAttributes2, wmdm.iwmdmstorage2_setattributes2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.redist: 
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
 - IWMDMStorage2.SetAttributes2
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage2::SetAttributes2


## -description



The <b>SetAttributes2</b> method sets extended attributes of the storage.




## -parameters




### -param dwAttributes [in]

<b>DWORD</b> specifying the base attributes defined in the <a href="https://msdn.microsoft.com/7484e29a-5faf-4a11-9fc1-75aa5c9d72ef">IWMDMStorage::SetAttributes</a> method.


### -param dwAttributesEx [in]

<b>DWORD</b> specifying extended attributes. Currently, no extended attributes are defined.


### -param pFormat [out]

Optional pointer to a <a href="https://msdn.microsoft.com/2128f07a-4858-49b7-b031-16d4a84c9d32">_ WAVEFORMATEX</a> structure that specifies audio information about the object. This parameter is ignored if the file is not audio.


### -param pVideoFormat [in]

Optional pointer to a <a href="https://msdn.microsoft.com/5a39d66e-8dbc-4572-8370-14f722b6c906">_VIDEOINFOHEADER</a> structure that specifies video information about the object. This parameter is ignored if the file is not video.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/1283a5b5-d893-4795-a50a-5a3bd6fce8d5">IWMDMStorage2 Interface</a>



<a href="https://msdn.microsoft.com/8212ab78-0a2a-41cd-8a7c-da6e3886b586">IWMDMStorage2::GetAttributes2</a>
 

 

