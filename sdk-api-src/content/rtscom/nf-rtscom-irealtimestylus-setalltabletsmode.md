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
 

 

