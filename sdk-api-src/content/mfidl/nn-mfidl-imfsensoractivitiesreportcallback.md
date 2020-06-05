---
UID: NN:mfidl.IMFSensorActivitiesReportCallback
title: IMFSensorActivitiesReportCallback (mfidl.h)
description: Interface implemented by the client to receive callbacks when sensor activity reports are available.helpviewer_keywords: ["IMFSensorActivitiesReportCallback","IMFSensorActivitiesReportCallback interface [Media Foundation]","IMFSensorActivitiesReportCallback interface [Media Foundation]","described","mf.imfsensoractivitiesreportcallback","mfidl/IMFSensorActivitiesReportCallback"]
old-location: mf\imfsensoractivitiesreportcallback.htm
tech.root: medfound
ms.assetid: 477B008D-7F0A-4084-BDFD-DF19E2A82817
ms.date: 12/05/2018
ms.keywords: IMFSensorActivitiesReportCallback, IMFSensorActivitiesReportCallback interface [Media Foundation], IMFSensorActivitiesReportCallback interface [Media Foundation],described, mf.imfsensoractivitiesreportcallback, mfidl/IMFSensorActivitiesReportCallback
f1_keywords:
- mfidl/IMFSensorActivitiesReportCallback
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.lib
- mfplat.dll
- mfplat.dll
- mfplat.dll.dll
api_name:
- IMFSensorActivitiesReportCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorActivitiesReportCallback interface


## -description


Interface implemented by the client to receive callbacks when sensor activity reports are available.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorActivitiesReportCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorActivitiesReportCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorActivitiesReportCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivitiesreportcallback-onactivitiesreport">OnActivitiesReport</a>
</td>
<td align="left" width="63%">
Raised by the media pipeline when a new <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a> is available.

</td>
</tr>
</table> 


## -remarks



Register the callback by passing an implementation of this interface into <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a>.



