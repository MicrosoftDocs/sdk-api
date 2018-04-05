---
UID: NS:textstor.TS_SELECTION_ACP
title: TS_SELECTION_ACP
author: windows-driver-content
description: The TS_SELECTION_ACP structure contains ACP-based text selection data.
old-location: tsf\ts_selection_acp.htm
old-project: TSF
ms.assetid: 739c87c5-3e9c-41f3-ad79-0b417347604b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: TS_SELECTION_ACP, TS_SELECTION_ACP structure [Text Services Framework], _tsf_ts_selection_acp_ref, textstor/TS_SELECTION_ACP, tsf.ts_selection_acp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_SELECTION_ACP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Textstor.h
api_name:
-	TS_SELECTION_ACP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TS_SELECTION_ACP structure


## -description



The <b>TS_SELECTION_ACP</b> structure contains ACP-based text selection data.




## -struct-fields




### -field acpStart

Contains the start position of the selection.


### -field acpEnd

Contains the end position of the selection.


### -field style

A <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure that contains additional selection data.


## -see-also




<a href="https://msdn.microsoft.com/e2052daf-4168-4266-ae8d-a09ecbfeb422">ITextStoreACP::GetSelection
      </a>



<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">
        ITextStoreACP::SetSelection
      </a>



<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">
        TS_SELECTIONSTYLE
      </a>
 

 

