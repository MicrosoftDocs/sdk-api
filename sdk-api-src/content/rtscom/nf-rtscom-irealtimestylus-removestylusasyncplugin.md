---
UID: NF:rtscom.IRealTimeStylus.RemoveStylusAsyncPlugin
title: IRealTimeStylus::RemoveStylusAsyncPlugin (rtscom.h)

description: Removes and optionally returns an IStylusAsyncPlugin with the specified index in the asynchronous plug-in collection.
old-location: tablet\irealtimestylus_removestylusasyncplugin.htm
tech.root: tablet
ms.assetid: 9c993147-3711-45ad-8996-e1434fd4b657

ms.date: 12/05/2018
ms.keywords: 9c993147-3711-45ad-8996-e1434fd4b657, IRealTimeStylus interface [Tablet PC],RemoveStylusAsyncPlugin method, IRealTimeStylus.RemoveStylusAsyncPlugin, IRealTimeStylus::RemoveStylusAsyncPlugin, RemoveStylusAsyncPlugin, RemoveStylusAsyncPlugin method [Tablet PC], RemoveStylusAsyncPlugin method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::RemoveStylusAsyncPlugin, tablet.irealtimestylus_removestylusasyncplugin
ms.topic: method
f1_keywords: 
 - "rtscom/IRealTimeStylus.RemoveStylusAsyncPlugin"
dev_langs:
 - c++
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
req.lib: 
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.RemoveStylusAsyncPlugin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylus::RemoveStylusAsyncPlugin


## -description



Removes and optionally returns an <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> with the specified index in the asynchronous plug-in collection.




## -parameters




### -param iIndex [in]

The index of the plug-in to be removed.


### -param ppiPlugin [in, out]

A pointer to the plug-in to remove. If you are not interested in receiving the pointer to the removed plug-in, pass <b>NULL</b> for this parameter.


## -returns



For a description of the return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removeallstylusasyncplugins">IRealTimeStylus::RemoveAllStylusAsyncPlugins Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removestylussyncplugin">IRealTimeStylus::RemoveStylusSyncPlugin Method</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
 

 

