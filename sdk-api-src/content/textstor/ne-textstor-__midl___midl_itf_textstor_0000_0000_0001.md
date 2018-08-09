---
UID: NE:textstor.__MIDL___MIDL_itf_textstor_0000_0000_0001
title: "__MIDL___MIDL_itf_textstor_0000_0000_0001"
author: windows-sdk-content
description: Elements of the TsActiveSelEnd enumeration specify which end of a text store selection is active.
old-location: tsf\tsactiveselend.htm
old-project: TSF
ms.assetid: 95695f10-2296-41fe-b2b4-efae548292bb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TS_AE_END, TS_AE_NONE, TS_AE_START, TsActiveSelEnd, TsActiveSelEnd enumeration [Text Services Framework], __MIDL___MIDL_itf_textstor_0000_0000_0001, _tsf_tsactiveselend_ref, textstor/TS_AE_END, textstor/TS_AE_NONE, textstor/TS_AE_START, textstor/TsActiveSelEnd, tsf.tsactiveselend
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: TsActiveSelEnd
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Textstor.h
api_name:
 - TsActiveSelEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_textstor_0000_0000_0001 enumeration


## -description


Elements of the <b>TsActiveSelEnd</b> enumeration specify which end of a text store selection is active.


## -enum-fields




### -field TS_AE_NONE

The selection has no active end. This is typical for all selections other than the default selection.


### -field TS_AE_START

The active end of the selection is at the start of the range of text.


### -field TS_AE_END

The active end of the selection is at the end of the range of text.


## -remarks



The active end of a selection is the end likely to respond to user actions. For example, in many applications, holding down the SHIFT key while using the arrow keys will change the selection. The end of the selection that moves is the active end of the selection.

This enumeration is used in the <a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/20d0efc2-604f-4ec6-820d-0f87a6d011b0">TS_SELECTIONSTYLE
      </a>
 

 

