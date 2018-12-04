---
UID: NS:commctrl.tagLHITTESTINFO
title: tagLHITTESTINFO
author: windows-sdk-content
description: Used to get information about the link corresponding to a given location.
old-location: controls\LHITTESTINFO.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\syslink\structures\lhittestinfo.htm
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PLHITTESTINFO, LHITTESTINFO, LHITTESTINFO structure [Windows Controls], PLHITTESTINFO, PLHITTESTINFO structure pointer [Windows Controls], commctrl/LHITTESTINFO, commctrl/PLHITTESTINFO, controls.LHITTESTINFO, controls.inet_LHITTESTINFO, inet_LHITTESTINFO, inet_LHITTESTINFO_cpp, tagLHITTESTINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Commctrl.h
api_name:
 - LHITTESTINFO
product: Windows
targetos: Windows
req.typenames: LHITTESTINFO, *PLHITTESTINFO
req.redist: 
---

# tagLHITTESTINFO structure


## -description


Used to get information about the link corresponding to a given location.



## -struct-fields




### -field pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

Location for the hit-test, in client coordinates (not screen coordinates).



### -field item

Type: <b><a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM</a></b>

Receives information about the link corresponding to <b>pt</b>.


## -remarks



To convert from screen coordinates to client coordinates, use <a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a>.

<div class="alert"><b>Note</b>  If the <a href="https://msdn.microsoft.com/a84c0388-26e7-4eda-9c6c-c5f64142d67a">LM_HITTEST</a> message succeeds, the system fills in <a href="https://msdn.microsoft.com/c3d62876-b92a-43b0-bc23-8b006847a474">LITEM.iLink</a> and <b>LITEM.szID</b>. If the <b>LM_HITTEST</b> message fails, do not assume that any information in <b>LITEM</b> is valid.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a84c0388-26e7-4eda-9c6c-c5f64142d67a">LM_HITTEST</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/5d3e65d1-e0c8-4063-b2e8-dd9f482d3378">ScreenToClient</a>
 

 

