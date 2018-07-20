---
UID: NF:mfidl.IMFSensorActivitiesReportCallback.OnActivitiesReport
title: IMFSensorActivitiesReportCallback::OnActivitiesReport
author: windows-sdk-content
description: Raised by the media pipeline when a new IMFSensorActivitiesReport is available.
old-location: mf\imfsensoractivitiesreportcallback_onactivitiesreport.htm
old-project: medfound
ms.assetid: B4D2332C-757F-4A2A-A12B-81BB503B02A4
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFSensorActivitiesReportCallback interface [Media Foundation],OnActivitiesReport method, IMFSensorActivitiesReportCallback.OnActivitiesReport, IMFSensorActivitiesReportCallback::OnActivitiesReport, OnActivitiesReport, OnActivitiesReport method [Media Foundation], OnActivitiesReport method [Media Foundation],IMFSensorActivitiesReportCallback interface, mf.imfsensoractivitiesreportcallback_onactivitiesreport, mfidl/IMFSensorActivitiesReportCallback::OnActivitiesReport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivitiesReportCallback::OnActivitiesReport


## -description


Raised by the media pipeline when a new <a href="https://msdn.microsoft.com/CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3">IMFSensorActivitiesReport</a> is available.


## -parameters




### -param sensorActivitiesReport






#### - pActivities [in]

Receives a pointer to the new <a href="https://msdn.microsoft.com/CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3">IMFSensorActivitiesReport</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/477B008D-7F0A-4084-BDFD-DF19E2A82817">IMFSensorActivitiesReportCallback</a>
 

 

