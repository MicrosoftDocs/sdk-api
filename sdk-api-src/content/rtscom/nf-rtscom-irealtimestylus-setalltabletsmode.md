---
UID: NF:rtscom.IRealTimeStylus.SetAllTabletsMode
title: IRealTimeStylus::SetAllTabletsMode
author: windows-driver-content
description: Sets the mode for the RealTimeStylus Class object to collect data from all digitizers.
old-location: tablet\irealtimestylus_setalltabletsmode.htm
old-project: tablet
ms.assetid: cb8b2a17-68b9-482b-b212-ad129522ff2e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IRealTimeStylus interface [Tablet PC],SetAllTabletsMode method, IRealTimeStylus.SetAllTabletsMode, IRealTimeStylus::SetAllTabletsMode, SetAllTabletsMode, SetAllTabletsMode method [Tablet PC], SetAllTabletsMode method [Tablet PC],IRealTimeStylus interface, cb8b2a17-68b9-482b-b212-ad129522ff2e, rtscom/IRealTimeStylus::SetAllTabletsMode, tablet.irealtimestylus_setalltabletsmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rtscom.h
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IRealTimeStylus.SetAllTabletsMode
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRealTimeStylus::SetAllTabletsMode


## -description



Sets the mode for the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object to collect data from all digitizers.




## -parameters




### -param fUseMouseForInput [in]

<b>TRUE</b> for both the mouse and stylus to be used for input; <b>FALSE</b> for the mouse not to be used as input.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method enables the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object to collect stylus events from any tablet attached to the Tablet PC. The <i>fUseMouseForInput</i> parameter specifies whether the mouse device, as well as the stylus, can be used for input.

If <a href="https://msdn.microsoft.com/7f3645fd-cb1e-4bd5-a995-d70197c61afc">IRealTimeStylus::SetSingleTabletMode Method</a> () was initially called and <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object is enabled, this call is invalid and TPC_E_INVALID_MODE HRESULT is returned.

<div class="alert"><b>Note</b>  The <b>IRealTimeStylus::SetAllTabletsMode Method</b> method will fail if the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> is enabled. On Microsoft Windows XP, this method will return <b>S_OK</b> but will have no effect. On Windows Vista, this method will return <b>E_INVALID_MODE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/38970fc0-ec4c-4068-a146-83edaa040c8c">IRealTimeStylus::GetTablet Method</a>



<a href="https://msdn.microsoft.com/7f3645fd-cb1e-4bd5-a995-d70197c61afc">IRealTimeStylus::SetSingleTabletMode Method</a>



<b>RealTimeStylus Class</b>
 

 

