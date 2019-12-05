---
UID: NF:shdeprecated.IBrowserService2.OnFrameWindowActivateBS
title: IBrowserService2::OnFrameWindowActivateBS (shdeprecated.h)
description: Deprecated. Calls the derived class from the base class in response to a subframe window being activated or deactivated. The derived class determines what to do in response to the action.
old-location: shell\IBrowserService2_OnFrameWindowActivateBS.htm
tech.root: shell
ms.assetid: 02134f59-c162-4247-9508-7ba40eec388b
ms.date: 12/05/2018
ms.keywords: FALSE, IBrowserService2 interface [Windows Shell],OnFrameWindowActivateBS method, IBrowserService2.OnFrameWindowActivateBS, IBrowserService2::OnFrameWindowActivateBS, OnFrameWindowActivateBS, OnFrameWindowActivateBS method [Windows Shell], OnFrameWindowActivateBS method [Windows Shell],IBrowserService2 interface, TRUE, shdeprecated/IBrowserService2::OnFrameWindowActivateBS, shell.IBrowserService2_OnFrameWindowActivateBS, zone_IBrowserService2_OnFrameWindowActivateBS
ms.topic: method
f1_keywords:
- shdeprecated/IBrowserService2.OnFrameWindowActivateBS
dev_langs:
- c++
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
- COM
api_location:
- Shdeprecated.h
api_name:
- IBrowserService2.OnFrameWindowActivateBS
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
---

# IBrowserService2::OnFrameWindowActivateBS


## -description


Deprecated. Calls the derived class from the base class in response to a subframe window being activated or deactivated. The derived class determines what to do in response to the action.


## -parameters




### -param fActive [in]

Type: <b>BOOL</b>

The state of the subframe window.



#### TRUE

The frame window is activating.



#### FALSE

The frame window is deactivating.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



