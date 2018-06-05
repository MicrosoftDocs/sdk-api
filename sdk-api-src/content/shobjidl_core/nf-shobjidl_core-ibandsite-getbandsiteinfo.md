---
UID: NF:shobjidl_core.IBandSite.GetBandSiteInfo
title: IBandSite::GetBandSiteInfo
author: windows-sdk-content
description: Gets information about a band in the band site.
old-location: shell\IBandSite_GetBandSiteInfo.htm
old-project: shell
ms.assetid: 5831de51-f785-430e-b7e6-f1f40a83357b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetBandSiteInfo, GetBandSiteInfo method [Windows Shell], GetBandSiteInfo method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],GetBandSiteInfo method, IBandSite.GetBandSiteInfo, IBandSite::GetBandSiteInfo, _win32_IBandSite_GetBandSiteInfo, shell.IBandSite_GetBandSiteInfo, shobjidl_core/IBandSite::GetBandSiteInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IBandSite.GetBandSiteInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
req.product: Outlook Express 6.0
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
 

 

