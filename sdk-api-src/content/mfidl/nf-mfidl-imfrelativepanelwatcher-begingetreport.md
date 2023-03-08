---
UID: NF:mfidl.IMFRelativePanelWatcher.BeginGetReport
title: IMFRelativePanelWatcher::BeginGetReport
ms.date: 11/4/2019
targetos: Windows
description: Begins an asynchronous request to get an IMFRelativePanelReport interface that represents the relative panel location.
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
req.lib: 
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
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFRelativePanelWatcher::BeginGetReport
f1_keywords:
 - IMFRelativePanelWatcher::BeginGetReport
 - mfidl/IMFRelativePanelWatcher::BeginGetReport
dev_langs:
 - c++
---

## -description

Begins an asynchronous request to get an [IMFRelativePanelReport](nn-mfidl-imfrelativepanelreport.md) interface that represents the relative panel location.

## -parameters

### -param pCallback

Pointer to the [IMFAsyncCallback](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface of a callback object. The caller must implement this interface.

### -param pState

Pointer to the IUnknown interface of a state object, defined by the caller. This parameter can be NULL. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

The function returns an **HRESULT**. Possible values include, but are not limited to, those in the following table.

| Return code | Description |
|--------------|------------------------|
|S_OK | The function succeeded.|

## -remarks

## -see-also

