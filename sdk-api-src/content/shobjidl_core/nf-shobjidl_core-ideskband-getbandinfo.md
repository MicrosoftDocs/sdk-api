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

# IDeskBand::GetBandInfo


## -description


Gets state information for a band object.
<div class="alert"><b>Important</b>  You should use <a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">thumbnail toolbars</a> in new development in place of desk bands, which are not supported as of Windows 7.</div><div> </div>

## -parameters




### -param dwBandID

Type: <b>DWORD</b>

The identifier of the band, assigned by the container. The band object can retain this value if it is required.


### -param dwViewMode

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


### -param pdbi

Type: <b><a href="https://msdn.microsoft.com/f44ef8a7-b05d-4908-95eb-b07d085e0c29">DESKBANDINFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/f44ef8a7-b05d-4908-95eb-b07d085e0c29">DESKBANDINFO</a> structure that receives the band information for the object. The <b>dwMask</b> member of this structure indicates the specific information that is being requested.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



