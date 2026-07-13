---
UID: NF:mfidl.MFCreateRelativePanelWatcher
title: MFCreateRelativePanelWatcher
ms.date: 11/4/2019
targetos: Windows
description: Creates a new instance of the **IMFRelativePanelWatcher** interface
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - MFCreateRelativePanelWatcher
f1_keywords:
 - MFCreateRelativePanelWatcher
 - mfidl/MFCreateRelativePanelWatcher
dev_langs:
 - c++
---

## -description

Creates a new instance of the **IMFRelativePanelWatcher** interface, which monitors the panel associated with the provided display monitor, so that the app receives notifications when the relative location of the panel changes.

## -parameters

### -param videoDeviceId

A string containing the symbolic link name of the video capture device.

### -param displayMonitorDeviceId

A string containing the symbolic link name of the display monitor device.

### -param ppRelativePanelWatcher

A pointer to an **IMFRelativePanelWatcher** interface representing the watcher.

## -returns

The function returns an **HRESULT**. Possible values include, but are not limited to, those in the following table.

| Return code | Description |
|--------------|------------------------|
|S_OK | The function succeeded.|

## -remarks

## -see-also

