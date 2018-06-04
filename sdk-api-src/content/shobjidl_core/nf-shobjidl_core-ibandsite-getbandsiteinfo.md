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

# IBandSite::GetBandSiteInfo


## -description


Gets information about a band in the band site.


## -parameters




### -param pbsinfo [in, out]

Type: <b><a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a>*</b>

The address of a <a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a> structure that contains
				the band site information for the object. The
				<b>dwMask</b> member of this structure
				specifies what information is being requested.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a>



<a href="https://msdn.microsoft.com/d7893136-a1a3-4c4b-b8f3-e4679710d827">IBandSite</a>



<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>
 

 

