---
UID: NE:rectypes.enumALT_BREAKS
title: ALT_BREAKS (rectypes.h)
author: windows-sdk-content
description: Specifiers how to create alternates from a best result string.
old-location: tablet\alt_breaks.htm
tech.root: tablet
ms.assetid: bca0466c-4262-41b9-b3bc-cec25df6e654
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ALT_BREAKS, ALT_BREAKS enumeration [Tablet PC], ALT_BREAKS_FULL, ALT_BREAKS_SAME, ALT_BREAKS_UNIQUE, bca0466c-4262-41b9-b3bc-cec25df6e654, rectypes/ALT_BREAKS, rectypes/ALT_BREAKS_FULL, rectypes/ALT_BREAKS_SAME, rectypes/ALT_BREAKS_UNIQUE, tablet.alt_breaks
ms.topic: enum
f1_keywords: 
 - "rectypes/ALT_BREAKS"
req.header: rectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - rectypes.h
api_name:
 - ALT_BREAKS
product: Windows
targetos: Windows
req.typenames: ALT_BREAKS
req.redist: 
ms.custom: 19H1
---

# ALT_BREAKS enumeration


## -description



Specifiers how to create alternates from a best result string.




## -enum-fields




### -field ALT_BREAKS_SAME

An alternate must use the same segment breaks as the best result string. For example, if you ask for an alternate list for the best result string of "together", the recognizer may return "Tunisia" but not "to get her". This is because "to get her" involves different segment breaks.


### -field ALT_BREAKS_UNIQUE

An alternate must have different segment breaks than the best result string. Only one such alternate is returned. For example, alternates for the best result string of "to get her" may include "to gather" and "together". However, "to got her" is not returned because it has the same segment break as "to get her".


### -field ALT_BREAKS_FULL

The top-rated alternates are returned regardless of segment breaks. Thus "together" may return "Tunisia", "to get her", and "to gather" among others. The alternates are returned in order of their rating, from best to worst.


## -remarks



Check the <a href="https://docs.microsoft.com/windows/desktop/api/rectypes/ns-rectypes-tagreco_attrs">dwRecoCapabilityFlags</a> member of the <b>RECO_ATTRS</b> structure to ensure the recognizer supports different alternate breaks.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms698163(v=vs.85)">GetAlternateList Function</a>
 

 

