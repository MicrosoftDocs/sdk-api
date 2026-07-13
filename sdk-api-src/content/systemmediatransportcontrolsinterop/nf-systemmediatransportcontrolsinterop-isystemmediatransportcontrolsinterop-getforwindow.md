---
UID: NF:systemmediatransportcontrolsinterop.ISystemMediaTransportControlsInterop.GetForWindow
title: ISystemMediaTransportControlsInterop::GetForWindow (systemmediatransportcontrolsinterop.h)
description: Gets an instance of the ISystemMediaTransportControls interface for the specified window.
helpviewer_keywords: ["GetForWindow","GetForWindow method","GetForWindow method","ISystemMediaTransportControlsInterop interface","ISystemMediaTransportControlsInterop interface","GetForWindow method","ISystemMediaTransportControlsInterop.GetForWindow","ISystemMediaTransportControlsInterop::GetForWindow","mediatransport.isystemmediatransportcontrolsinterop_getforwindow","systemmediatransportcontrolsinterop/ISystemMediaTransportControlsInterop::GetForWindow"]
old-location: mediatransport\isystemmediatransportcontrolsinterop_getforwindow.htm
tech.root: winrt
ms.assetid: 7E878C3B-4CE9-4DED-8082-8E37266FE8AF
ms.date: 12/05/2018
ms.keywords: GetForWindow, GetForWindow method, GetForWindow method,ISystemMediaTransportControlsInterop interface, ISystemMediaTransportControlsInterop interface,GetForWindow method, ISystemMediaTransportControlsInterop.GetForWindow, ISystemMediaTransportControlsInterop::GetForWindow, mediatransport.isystemmediatransportcontrolsinterop_getforwindow, systemmediatransportcontrolsinterop/ISystemMediaTransportControlsInterop::GetForWindow
req.header: systemmediatransportcontrolsinterop.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISystemMediaTransportControlsInterop::GetForWindow
 - systemmediatransportcontrolsinterop/ISystemMediaTransportControlsInterop::GetForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - systemmediatransportcontrolsinterop.h
api_name:
 - ISystemMediaTransportControlsInterop.GetForWindow
---

# ISystemMediaTransportControlsInterop::GetForWindow


## -description

Gets an instance of the <a href="/previous-versions/windows/desktop/mediatransport/isystemmediatransportcontrols">ISystemMediaTransportControls</a> interface for the specified window.

## -parameters

### -param appWindow

The top-level app window for which the <a href="/previous-versions/windows/desktop/mediatransport/isystemmediatransportcontrols">ISystemMediaTransportControls</a> interface is retrieved.

### -param riid

A reference to the IID of the interface to retrieve.

### -param mediaTransportControl [out]

Receives the <a href="/previous-versions/windows/desktop/mediatransport/isystemmediatransportcontrols">ISystemMediaTransportControls</a> that corresponds to the <i>appWindow</i> window.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

The <i>appWindow</i> parameter must refer to a top-level window that belongs to the calling process.

## -see-also

<a href="/windows/win32/api/systemmediatransportcontrolsinterop/nn-systemmediatransportcontrolsinterop-isystemmediatransportcontrolsinterop">ISystemMediaTransportControlsInterop</a>