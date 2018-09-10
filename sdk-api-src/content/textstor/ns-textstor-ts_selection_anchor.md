---
UID: NS:textstor.TS_SELECTION_ANCHOR
title: TS_SELECTION_ANCHOR
author: windows-sdk-content
description: The TS_SELECTION_ANCHOR structure contains anchor-based text selection data.
old-location: tsf\ts_selection_anchor.htm
tech.root: TSF
ms.assetid: 56fbe145-1972-4b44-a730-17860e428dd0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TS_SELECTION_ANCHOR, TS_SELECTION_ANCHOR structure [Text Services Framework], _tsf_ts_selection_anchor_ref, textstor/TS_SELECTION_ANCHOR, tsf.ts_selection_anchor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TS_SELECTION_ANCHOR
product: Windows
targetos: Windows
req.typenames: TS_SELECTION_ANCHOR
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TS_SELECTION_ANCHOR structure


## -description



The <b>TS_SELECTION_ANCHOR</b> structure contains anchor-based text selection data.




## -struct-fields




### -field paStart

Contains the start anchor of the selection.


### -field paEnd

Contains the end anchor of the selection.


### -field style

A <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure that contains additional selection data.


## -see-also




<a href="https://msdn.microsoft.com/df1b21b7-b539-4546-96be-243a8e7ea75a">ITextStoreAnchor::GetSelection
      </a>



<a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">ITextStoreAnchor::SetSelection
      </a>



<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE
      </a>
 

 

