---
UID: NF:mfidl.IMFRelativePanelWatcher.EndGetReport
title: IMFRelativePanelWatcher::EndGetReport
ms.date: 11/4/2019
targetos: Windows
description: Ends an asynchronous request to get an IMFRelativePanelReport interface that represents the relative panel location.
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
 - IMFRelativePanelWatcher::EndGetReport
f1_keywords:
 - IMFRelativePanelWatcher::EndGetReport
 - mfidl/IMFRelativePanelWatcher::EndGetReport
dev_langs:
 - c++
---

## -description

Ends an asynchronous request to get an [IMFRelativePanelReport](nn-mfidl-imfrelativepanelreport.md) interface that represents the relative panel location.

## -parameters

### -param pResult

Pointer to the [IMFAsyncResult](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface. Pass in the same pointer that your callback object received in the Invoke method.

### -param ppRelativePanelReport

A pointer to he [IMFRelativePanelReport](nn-mfidl-imfrelativepanelreport.md) interface that represents the relative panel location.

## -returns

The function returns an **HRESULT**. Possible values include, but are not limited to, those in the following table.

| Return code | Description |
|--------------|------------------------|
|S_OK | The function succeeded.|

## -remarks

## -see-also

