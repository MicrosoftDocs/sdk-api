---
UID: NF:shobjidl_core.IBandSite.GetBandObject
title: IBandSite::GetBandObject
author: windows-sdk-content
description: Gets a specified band object from a band site.
old-location: shell\IBandSite_GetBandObject.htm
tech.root: shell
ms.assetid: e6eba36d-5fc8-4b79-8129-1e07c5cc5b5f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetBandObject, GetBandObject method [Windows Shell], GetBandObject method [Windows Shell],IBandSite interface, IBandSite interface [Windows Shell],GetBandObject method, IBandSite.GetBandObject, IBandSite::GetBandObject, _win32_IBandSite_GetBandObject, shell.IBandSite_GetBandObject, shobjidl_core/IBandSite::GetBandObject
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
 - IBandSite.GetBandObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IBandSite.GetBandObject
: 
---

# IBandSite::GetBandObject


## -description


Gets a specified band object from a band site.


## -parameters




### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band object to get.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the object to obtain.


### -param ppv [out]

Type: <b>VOID**</b>

The address of a pointer variable that receives a pointer
				to the object requested.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/d7893136-a1a3-4c4b-b8f3-e4679710d827">IBandSite</a>



<a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>
 

 

