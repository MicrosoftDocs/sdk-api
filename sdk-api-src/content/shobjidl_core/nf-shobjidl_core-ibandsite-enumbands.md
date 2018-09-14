---
UID: NF:shobjidl_core.IBandSite.EnumBands
title: IBandSite::EnumBands
author: windows-sdk-content
description: Enumerates the bands in a band site.
old-location: shell\IBandSite_EnumBands.htm
tech.root: shell
ms.assetid: d92ead78-9d58-48fe-ad93-33b2dbcbda68
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: EnumBands, EnumBands method [Windows Shell], EnumBands method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],EnumBands method, IBandSite.EnumBands, IBandSite::EnumBands, _win32_IBandSite_EnumBands, shell.IBandSite_EnumBands, shobjidl_core/IBandSite::EnumBands
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
 - IBandSite.EnumBands
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandSite::EnumBands


## -description


Enumerates the bands in a band site.


## -parameters




### -param uBand [in]

Type: <b>UINT</b>

Call the method with this parameter starting at 0 to
				begin enumerating.  If this parameter is -1, the
        <i>pdwBandID</i>parameter is ignored and this method returns the count of the
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
 

 

