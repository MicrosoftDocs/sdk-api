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

# IDeskBandInfo::GetDefaultBandWidth


## -description


<p class="CCE_Message">[<b>GetDefaultBandWidth</b> may be altered or unavailable in subsequent versions of the operating system or product.]

Gets the band width that the bandsite initially uses to set the default width when the band is added.


## -parameters




### -param dwBandID [in]

Type: <b>DWORD</b>

The band ID.


### -param dwViewMode [in]

Type: <b>DWORD</b>

The view mode of the band object. One of the following values: 



#### DBIF_VIEWMODE_NORMAL

The band object is being displayed in a horizontal band.



#### DBIF_VIEWMODE_VERTICAL

The band object is being displayed in a vertical band.



#### DBIF_VIEWMODE_FLOATING

The band object is being displayed in a floating band.



#### DBIF_VIEWMODE_TRANSPARENT

The band object is being displayed in a transparent band.


### -param pnWidth [out]

Type: <b>int*</b>

A pointer to the band width.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



