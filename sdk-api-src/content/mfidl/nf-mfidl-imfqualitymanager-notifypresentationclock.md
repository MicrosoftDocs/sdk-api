---
UID: NF:mfidl.IMFQualityManager.NotifyPresentationClock
title: IMFQualityManager::NotifyPresentationClock (mfidl.h)
description: Called when the Media Session selects a presentation clock.
helpviewer_keywords: ["IMFQualityManager interface [Media Foundation]","NotifyPresentationClock method","IMFQualityManager.NotifyPresentationClock","IMFQualityManager::NotifyPresentationClock","NotifyPresentationClock","NotifyPresentationClock method [Media Foundation]","NotifyPresentationClock method [Media Foundation]","IMFQualityManager interface","b358d98e-7b02-4c58-b556-cfa15436e435","mf.imfqualitymanager_notifypresentationclock","mfidl/IMFQualityManager::NotifyPresentationClock"]
old-location: mf\imfqualitymanager_notifypresentationclock.htm
tech.root: mf
ms.assetid: b358d98e-7b02-4c58-b556-cfa15436e435
ms.date: 12/05/2018
ms.keywords: IMFQualityManager interface [Media Foundation],NotifyPresentationClock method, IMFQualityManager.NotifyPresentationClock, IMFQualityManager::NotifyPresentationClock, NotifyPresentationClock, NotifyPresentationClock method [Media Foundation], NotifyPresentationClock method [Media Foundation],IMFQualityManager interface, b358d98e-7b02-4c58-b556-cfa15436e435, mf.imfqualitymanager_notifypresentationclock, mfidl/IMFQualityManager::NotifyPresentationClock
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
 - IMFQualityManager::NotifyPresentationClock
 - mfidl/IMFQualityManager::NotifyPresentationClock
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
 - IMFQualityManager.NotifyPresentationClock
---

# IMFQualityManager::NotifyPresentationClock


## -description

Called when the Media Session selects a presentation clock.

## -parameters

### -param pClock [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock">IMFPresentationClock</a> interface of the presentation clock. If this parameter is <b>NULL</b>, the quality manager should release any references to the presentation clock.

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

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager">IMFQualityManager</a>