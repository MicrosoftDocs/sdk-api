---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IBandSite::EnumBands


## -description


Enumerates the bands in a band site.


## -parameters




### -param uBand [in]

Type: <b>UINT</b>

Call the method with this parameter starting at 0 to
				begin enumerating.  If this parameter is -1, the
        <i>pdwBandID</i>
				parameter is ignored and this method returns the count of the
				bands in the band site.


### -param pdwBandID [out]

Type: <b>DWORD*</b>

The address of a band ID variable that receives the band ID.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code for errors.
				If the first parameter is -1, the count of the bands in the band site
				is returned.




## -see-also




<a href="https://msdn.microsoft.com/d7893136-a1a3-4c4b-b8f3-e4679710d827">IBandSite</a>



<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>
 

 

