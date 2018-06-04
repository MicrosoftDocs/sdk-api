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

# IOpenControlPanel::GetCurrentView


## -description


Gets the most recent Control Panel view: Classic view or Category view.


## -parameters




### -param pView [out]

Type: <b>CPVIEW*</b>

A pointer that receives the most recent view. Valid values are as follows:



#### CPVIEW_CLASSIC (0x0)

0x0. Classic view.



#### CPVIEW_ALLITEMS (CPVIEW_CLASSIC)

0x0. <b>Windows 7 and later</b>. Equivalent to CPVIEW_CLASSIC.



#### CPVIEW_CATEGORY (0x1)

0x1. Category view.



#### CPVIEW_HOME (0x1)

0x1. <b>Windows 7 and later</b>. Equivalent to CPVIEW_CATEGORY.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



