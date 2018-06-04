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

# IBandSite::QueryBand


## -description


Gets information about a band in a band site.


## -parameters




### -param dwBandID [in]

Type: <b>DWORD</b>

The ID of the band object to query.


### -param ppstb [out, optional]

Type: <b><a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a>**</b>

Address of an <a href="https://msdn.microsoft.com/eb9f7f2a-a6be-4527-8a32-325dad4c8000">IDeskBand</a> interface pointer that, when this method returns successfully, points to the <b>IDeskBand</b> object that represents the band. This value can be <b>NULL</b>.


### -param pdwState [out, optional]

Type: <b>DWORD*</b>

Pointer to a <b>DWORD</b> value that, when this method returns successfully, receives the state of the band object. This state is a combination of BSSF_VISIBLE, BSSF_NOTITLE, and BSSF_UNDELETEABLE. See <a href="https://msdn.microsoft.com/86e4afce-594a-441e-b6d9-ce05c8234150">BANDSITEINFO</a> for more information on those flags. This value can be <b>NULL</b> if the state information is not needed.


### -param pszName [out]

Type: <b>LPWSTR</b>

Pointer to a buffer of <i>cchName</i> Unicode characters that, when this method returns successfully, receives the name of the band object.


### -param cchName [in]

Type: <b>int</b>

The size of the <i>pszName</i> buffer, in characters.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



