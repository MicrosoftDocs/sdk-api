---
UID: NF:mfsharingengine.IPlayToControl.Connect
title: IPlayToControl::Connect
author: windows-sdk-content
description: Connects the media element to the media sharing engine.
old-location: mf\iplaytocontrol_connect.htm
old-project: medfound
ms.assetid: 5252DC51-E1EF-4A61-A2BD-682F51DC219B
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Connect, Connect method [Media Foundation], Connect method [Media Foundation],IPlayToControl interface, IPlayToControl interface [Media Foundation],Connect method, IPlayToControl.Connect, IPlayToControl::Connect, mf.iplaytocontrol_connect, mfsharingengine/IPlayToControl::Connect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PLAYTO_SOURCE_CREATEFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IPlayToControl.Connect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPlayToControl::Connect


## -description


Connects the media element to the media sharing engine.


## -parameters




### -param pFactory [in]

A pointer to the <a href="https://msdn.microsoft.com/191CB50C-8CBB-470F-B558-F3A9EE554DA3">IMFSharingEngineClassFactory</a> interface. The media element uses this interface to create the Sharing Engine.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/53355EEA-559B-4803-89F6-D454E15F9254">IPlayToControl</a>
 

 

