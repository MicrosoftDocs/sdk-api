---
UID: NF:mfsharingengine.IPlayToControl.Connect
title: IPlayToControl::Connect (mfsharingengine.h)
description: Connects the media element to the media sharing engine.
helpviewer_keywords: ["Connect","Connect method [Media Foundation]","Connect method [Media Foundation]","IPlayToControl interface","IPlayToControl interface [Media Foundation]","Connect method","IPlayToControl.Connect","IPlayToControl::Connect","mf.iplaytocontrol_connect","mfsharingengine/IPlayToControl::Connect"]
old-location: mf\iplaytocontrol_connect.htm
tech.root: mf
ms.assetid: 5252DC51-E1EF-4A61-A2BD-682F51DC219B
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Media Foundation], Connect method [Media Foundation],IPlayToControl interface, IPlayToControl interface [Media Foundation],Connect method, IPlayToControl.Connect, IPlayToControl::Connect, mf.iplaytocontrol_connect, mfsharingengine/IPlayToControl::Connect
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPlayToControl::Connect
 - mfsharingengine/IPlayToControl::Connect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IPlayToControl.Connect
---

# IPlayToControl::Connect


## -description

Connects the media element to the media sharing engine.

## -parameters

### -param pFactory [in]

A pointer to the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory">IMFSharingEngineClassFactory</a> interface. The media element uses this interface to create the Sharing Engine.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol">IPlayToControl</a>