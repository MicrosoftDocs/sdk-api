---
UID: NF:mfidl.IMFSensorActivitiesReportCallback.OnActivitiesReport
title: IMFSensorActivitiesReportCallback::OnActivitiesReport (mfidl.h)
description: Raised by the media pipeline when a new IMFSensorActivitiesReport is available.
helpviewer_keywords: ["IMFSensorActivitiesReportCallback interface [Media Foundation]","OnActivitiesReport method","IMFSensorActivitiesReportCallback.OnActivitiesReport","IMFSensorActivitiesReportCallback::OnActivitiesReport","OnActivitiesReport","OnActivitiesReport method [Media Foundation]","OnActivitiesReport method [Media Foundation]","IMFSensorActivitiesReportCallback interface","mf.imfsensoractivitiesreportcallback_onactivitiesreport","mfidl/IMFSensorActivitiesReportCallback::OnActivitiesReport"]
old-location: mf\imfsensoractivitiesreportcallback_onactivitiesreport.htm
tech.root: mf
ms.assetid: B4D2332C-757F-4A2A-A12B-81BB503B02A4
ms.date: 12/05/2018
ms.keywords: IMFSensorActivitiesReportCallback interface [Media Foundation],OnActivitiesReport method, IMFSensorActivitiesReportCallback.OnActivitiesReport, IMFSensorActivitiesReportCallback::OnActivitiesReport, OnActivitiesReport, OnActivitiesReport method [Media Foundation], OnActivitiesReport method [Media Foundation],IMFSensorActivitiesReportCallback interface, mf.imfsensoractivitiesreportcallback_onactivitiesreport, mfidl/IMFSensorActivitiesReportCallback::OnActivitiesReport
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorActivitiesReportCallback::OnActivitiesReport
 - mfidl/IMFSensorActivitiesReportCallback::OnActivitiesReport
dev_langs:
 - c++
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
 - IMFSensorActivitiesReportCallback.OnActivitiesReport
---

# IMFSensorActivitiesReportCallback::OnActivitiesReport


## -description

Raised by the media pipeline when a new <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a> is available.

## -parameters

### -param sensorActivitiesReport [in]

Receives a pointer to the new <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport">IMFSensorActivitiesReport</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a>