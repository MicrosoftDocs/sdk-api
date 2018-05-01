---
UID: NN:mfidl.IMFSensorActivitiesReport
title: IMFSensorActivitiesReport
author: windows-driver-content
description: Provides access to IMFSensorActivityReport objects that describe the current activity of a sensor.
old-location: mf\imfsensoractivitiesreport.htm
old-project: medfound
ms.assetid: CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFSensorActivitiesReport, IMFSensorActivitiesReport interface [Media Foundation], IMFSensorActivitiesReport interface [Media Foundation], described, mf.imfsensoractivitiesreport, mfidl/IMFSensorActivitiesReport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorActivitiesReport
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivitiesReport interface


## -description


Provides access to <a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a> objects that describe the current activity of a sensor.


## -remarks



Register to receive sensor activities reports by implementing the <a href="https://msdn.microsoft.com/477B008D-7F0A-4084-BDFD-DF19E2A82817">IMFSensorActivitiesReportCallback</a> interface and passing the implementation into <a href="https://msdn.microsoft.com/852395EE-AA84-4C61-A55F-E8D925FA1447">MFCreateSensorActivityMonitor</a>.



