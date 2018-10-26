---
UID: NF:shobjidl_core.IBandSite.SetBandSiteInfo
title: IBandSite::SetBandSiteInfo
author: windows-sdk-content
description: Sets information about the band site.
old-location: shell\IBandSite_SetBandSiteInfo.htm
tech.root: shell
ms.assetid: 2658a49d-d60f-483b-bbe1-e1390e9dc35e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IBandSite interface [Windows Shell],SetBandSiteInfo method, IBandSite.SetBandSiteInfo, IBandSite::SetBandSiteInfo, SetBandSiteInfo, SetBandSiteInfo method [Windows Shell], SetBandSiteInfo method [Windows Shell],IBandSite interface, _win32_IBandSite_SetBandSiteInfo, shell.IBandSite_SetBandSiteInfo, shobjidl_core/IBandSite::SetBandSiteInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shldisp.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IBandSite.SetBandSiteInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandSite::SetBandSiteInfo


## -description


Sets information about the band site.


## -parameters




### -param pbsinfo [in]

Type: <b><a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a>*</b>

The address of a <a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a> structure that receives
				the band site information for the object. The
				<b>dwMask</b> member of this structure
				specifies what information is being set.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d7893136-a1a3-4c4b-b8f3-e4679710d827">IBandSite</a>



<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>
 

 

