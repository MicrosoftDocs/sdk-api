---
UID: NF:mfidl.IMFQualityManager.NotifyProcessInput
title: IMFQualityManager::NotifyProcessInput (mfidl.h)
description: Called when the media processor is about to deliver an input sample to a pipeline component.
helpviewer_keywords: ["IMFQualityManager interface [Media Foundation]","NotifyProcessInput method","IMFQualityManager.NotifyProcessInput","IMFQualityManager::NotifyProcessInput","NotifyProcessInput","NotifyProcessInput method [Media Foundation]","NotifyProcessInput method [Media Foundation]","IMFQualityManager interface","c6e35d03-ca83-4078-bcc1-b9c1d988de01","mf.imfqualitymanager_notifyprocessinput","mfidl/IMFQualityManager::NotifyProcessInput"]
old-location: mf\imfqualitymanager_notifyprocessinput.htm
tech.root: mf
ms.assetid: c6e35d03-ca83-4078-bcc1-b9c1d988de01
ms.date: 12/05/2018
ms.keywords: IMFQualityManager interface [Media Foundation],NotifyProcessInput method, IMFQualityManager.NotifyProcessInput, IMFQualityManager::NotifyProcessInput, NotifyProcessInput, NotifyProcessInput method [Media Foundation], NotifyProcessInput method [Media Foundation],IMFQualityManager interface, c6e35d03-ca83-4078-bcc1-b9c1d988de01, mf.imfqualitymanager_notifyprocessinput, mfidl/IMFQualityManager::NotifyProcessInput
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFQualityManager::NotifyProcessInput
 - mfidl/IMFQualityManager::NotifyProcessInput
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFQualityManager.NotifyProcessInput
---

# IMFQualityManager::NotifyProcessInput


## -description

Called when the media processor is about to deliver an input sample to a pipeline component.

## -parameters

### -param pNode [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode">IMFTopologyNode</a> interface of the topology node that represents the pipeline component.

### -param lInputIndex [in]

Index of the input stream on the topology node.

### -param pSample [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the input sample.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is called for every sample passing through every pipeline component. Therefore, the method must return quickly to avoid introducing too much latency into the pipeline.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>