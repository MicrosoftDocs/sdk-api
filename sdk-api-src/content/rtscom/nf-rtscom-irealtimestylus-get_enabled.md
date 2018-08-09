---
UID: NF:rtscom.IRealTimeStylus.get_Enabled
title: IRealTimeStylus::get_Enabled
author: windows-sdk-content
description: Gets or sets a value that specifies whether the RealTimeStylus object collects tablet pen data.
old-location: tablet\irealtimestylus_enabled.htm
old-project: tablet
ms.assetid: e96e27d7-b453-49a7-b684-b3dd5f94c378
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Enabled property [Tablet PC], Enabled property [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],Enabled property, IRealTimeStylus.Enabled, IRealTimeStylus.get_Enabled, IRealTimeStylus.put_Enabled, IRealTimeStylus::Enabled, IRealTimeStylus::get_Enabled, IRealTimeStylus::put_Enabled, e96e27d7-b453-49a7-b684-b3dd5f94c378, get_Enabled, rtscom/IRealTimeStylus::Enabled, rtscom/IRealTimeStylus::get_Enabled, rtscom/IRealTimeStylus::put_Enabled, tablet.irealtimestylus_enabled
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.Enabled
 - IRealTimeStylus.get_Enabled
 - IRealTimeStylus.put_Enabled
 - IRealTimeStylus.get_Enabled
 - IRealTimeStylus.put_Enabled
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylus::get_Enabled


## -description



Gets or sets a value that specifies whether the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object collects tablet pen data.



This property is read/write.


## -parameters


## -remarks



Multiple <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> objects can exist on the same window provided they are not enabled with overlapping window input rectangles. Enabled <b>RealTimeStylus</b> objects on the same window with overlapping input rectangles result in undetermined behavior.

<div class="alert"><b>Note</b>  An overlap can occur without an error if only one of the input rectangles is enabled at any one time.</div>
<div> </div>
A child <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object must be connected to be enabled.

Although a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object can be enabled when it has no plug-ins attached to it, it must have at least one plug-in to be useful.

You receive no events when an object is not enabled.

When the <b>IRealTimeStylus::Enabled Property</b> of a container control is set to <b>false</b>, all of its contained controls are also disabled.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/9d216853-9103-4027-a724-f35d84553a9b">IRealTimeStylus::AddCustomStylusDataToQueue Method</a>



<a href="https://msdn.microsoft.com/1e838591-ce9e-4f3f-9b5e-b8414faac6ba">IRealTimeStylus::GetStyluses Method</a>



<a href="https://msdn.microsoft.com/9f4cc882-c25f-4862-8b78-4db108d0b5d4">IRealTimeStylus::GetTabletContextIdFromTablet Method</a>



<a href="https://msdn.microsoft.com/be736eaf-8632-4e71-b1d8-c851a9d417e5">IRealTimeStylus::GetTabletFromTabletContextId Method</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

