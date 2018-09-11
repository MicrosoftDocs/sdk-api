---
UID: NF:shobjidl_core.IBandSite.SetBandState
title: IBandSite::SetBandState
author: windows-sdk-content
description: Set the state of a band in the band site.
old-location: shell\IBandSite_SetBandState.htm
tech.root: shell
ms.assetid: d327f0fe-7d61-4edd-aff3-f4507763d751
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBandSite interface [Windows Shell],SetBandState method, IBandSite.SetBandState, IBandSite::SetBandState, SetBandState, SetBandState method [Windows Shell], SetBandState method [Windows Shell],IBandSite interface, _win32_IBandSite_SetBandState, shell.IBandSite_SetBandState, shobjidl_core/IBandSite::SetBandState
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
 - IBandSite.SetBandState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBandSite::SetBandState


## -description


Set the state of a band in the band site.


## -parameters




### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band to set.  If this parameter is -1, then
				set the state of all bands in the band site.


### -param dwMask [in]

Type: <b>DWORD</b>

The mask of the states to set.


### -param dwState [in]

Type: <b>DWORD</b>

The state values to be set. These are combinations of
				BSSF_* flags. For more information, see <a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a>



<a href="https://msdn.microsoft.com/d7893136-a1a3-4c4b-b8f3-e4679710d827">IBandSite</a>



<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>
 

 

