---
UID: NF:rtscom.IRealTimeStylus.RemoveStylusAsyncPlugin
title: IRealTimeStylus::RemoveStylusAsyncPlugin
author: windows-driver-content
description: Removes and optionally returns an IStylusAsyncPlugin with the specified index in the asynchronous plug-in collection.
old-location: tablet\irealtimestylus_removestylusasyncplugin.htm
old-project: tablet
ms.assetid: 9c993147-3711-45ad-8996-e1434fd4b657
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 9c993147-3711-45ad-8996-e1434fd4b657, IRealTimeStylus interface [Tablet PC],RemoveStylusAsyncPlugin method, IRealTimeStylus.RemoveStylusAsyncPlugin, IRealTimeStylus::RemoveStylusAsyncPlugin, RemoveStylusAsyncPlugin, RemoveStylusAsyncPlugin method [Tablet PC], RemoveStylusAsyncPlugin method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::RemoveStylusAsyncPlugin, tablet.irealtimestylus_removestylusasyncplugin
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
-	IRealTimeStylus.RemoveStylusAsyncPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRealTimeStylus::RemoveStylusAsyncPlugin


## -description



Removes and optionally returns an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> with the specified index in the asynchronous plug-in collection.




## -parameters




### -param iIndex [in]

The index of the plug-in to be removed.


### -param ppiPlugin [in, out]

A pointer to the plug-in to remove. If you are not interested in receiving the pointer to the removed plug-in, pass <b>NULL</b> for this parameter.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/98b97156-f181-45f4-9cfb-13816f8042e6">IRealTimeStylus::RemoveAllStylusAsyncPlugins Method</a>



<a href="https://msdn.microsoft.com/5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8">IRealTimeStylus::RemoveStylusSyncPlugin Method</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 

