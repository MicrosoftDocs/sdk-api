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

# GetThemeAnimationTransform function


## -description


Gets an animation transform operation
based on storyboard id, target id and transform
index.


## -parameters




### -param hTheme [in]

An opened theme handle.


### -param iStoryboardId [in]

A predefined storyboard identifier.


### -param iTargetId [in]

A predefined target identifier.


### -param dwTransformIndex [in]

The zero-based index of a transform operation.


### -param pTransform [out]

A pointer to a buffer to receive a transform structure.


### -param cbSize [in]

The byte size of the buffer pointed by <i>pTransform</i>.


### -param pcbSizeOut [out]

The                                    byte  size of a transform operation structure.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



