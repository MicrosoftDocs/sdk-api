---
UID: NN:mfidl.IMFSensorActivitiesReport
title: IMFSensorActivitiesReport (mfidl.h)
description: Provides access to IMFSensorActivityReport objects that describe the current activity of a sensor.
helpviewer_keywords: ["IMFSensorActivitiesReport","IMFSensorActivitiesReport interface [Media Foundation]","IMFSensorActivitiesReport interface [Media Foundation]","described","mf.imfsensoractivitiesreport","mfidl/IMFSensorActivitiesReport"]
old-location: mf\imfsensoractivitiesreport.htm
tech.root: mf
ms.assetid: CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3
ms.date: 12/05/2018
ms.keywords: IMFSensorActivitiesReport, IMFSensorActivitiesReport interface [Media Foundation], IMFSensorActivitiesReport interface [Media Foundation],described, mf.imfsensoractivitiesreport, mfidl/IMFSensorActivitiesReport
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
 - IMFSensorActivitiesReport
 - mfidl/IMFSensorActivitiesReport
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
 - IMFSensorActivitiesReport
---

# IMFSensorActivitiesReport interface


## -description

Provides access to <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a> objects that describe the current activity of a sensor.

## -inheritance

The <b>IMFSensorActivitiesReport</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorActivitiesReport</b> also has these types of members:

## -remarks

Register to receive sensor activities reports by implementing the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback">IMFSensorActivitiesReportCallback</a> interface and passing the implementation into <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatesensoractivitymonitor">MFCreateSensorActivityMonitor</a>.
