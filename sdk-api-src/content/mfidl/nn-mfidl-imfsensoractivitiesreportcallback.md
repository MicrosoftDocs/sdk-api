---
UID: NN:mfidl.IMFSensorActivitiesReportCallback
title: IMFSensorActivitiesReportCallback (mfidl.h)
description: Interface implemented by the client to receive callbacks when sensor activity reports are available.
helpviewer_keywords: ["IMFSensorActivitiesReportCallback","IMFSensorActivitiesReportCallback interface [Media Foundation]","IMFSensorActivitiesReportCallback interface [Media Foundation]","described","mf.imfsensoractivitiesreportcallback","mfidl/IMFSensorActivitiesReportCallback"]
old-location: mf\imfsensoractivitiesreportcallback.htm
tech.root: mf
ms.assetid: 477B008D-7F0A-4084-BDFD-DF19E2A82817
ms.date: 12/05/2018
ms.keywords: IMFSensorActivitiesReportCallback, IMFSensorActivitiesReportCallback interface [Media Foundation], IMFSensorActivitiesReportCallback interface [Media Foundation],described, mf.imfsensoractivitiesreportcallback, mfidl/IMFSensorActivitiesReportCallback
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
 - IMFSensorActivitiesReportCallback
 - mfidl/IMFSensorActivitiesReportCallback
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
 - IMFSensorActivitiesReportCallback
---

# IMFSensorActivitiesReportCallback interface


## -description

Interface implemented by the client to receive callbacks when sensor activity reports are available.

## -inheritance

The <b>IMFSensorActivitiesReportCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorActivitiesReportCallback</b> also has these types of members:

## -remarks

Register the callback by passing an implementation of this interface into <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a>.
