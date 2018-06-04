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

# ICDBurnExt::GetSupportedActionTypes


## -description


Determines the supported data type for a CD writing extension.


## -parameters




### -param pdwActions [out]

Type: <b>CDBE_ACTIONS*</b>

One of the following values indicating the supported type.



#### CDBE_TYPE_MUSIC (0x00000001)

0x00000001. Music files are supported. The CD writing extension is invoked for the <b>Copy to audio CD</b> task in the My Music folder.



#### CDBE_TYPE_DATA (0x00000002)

0x00000002. Data files are supported. The CD writing extension is excluded from <b>Copy to audio CD</b>.



#### CDBE_TYPE_ALL ((int)0xFFFFFFFF)

(int)0xFFFFFFFF. All files are supported. The CD writing extension is invoked for the <b>Copy to audio CD</b> task in the My Music folder.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



