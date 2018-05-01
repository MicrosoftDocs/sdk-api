---
UID: NN:mfidl.IMFSensorActivitiesReportCallback
title: IMFSensorActivitiesReportCallback
author: windows-driver-content
description: Interface implemented by the client to receive callbacks when sensor activity reports are available.
old-location: mf\imfsensoractivitiesreportcallback.htm
old-project: medfound
ms.assetid: 477B008D-7F0A-4084-BDFD-DF19E2A82817
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFSensorActivitiesReportCallback, IMFSensorActivitiesReportCallback interface [Media Foundation], IMFSensorActivitiesReportCallback interface [Media Foundation], described, mf.imfsensoractivitiesreportcallback, mfidl/IMFSensorActivitiesReportCallback
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
-	IMFSensorActivitiesReportCallback
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivitiesReportCallback interface


## -description


Interface implemented by the client to receive callbacks when sensor activity reports are available.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorActivitiesReportCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorActivitiesReportCallback</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B4D2332C-757F-4A2A-A12B-81BB503B02A4">OnActivitiesReport</a>
</td>
<td align="left" width="63%">
Raised by the media pipeline when a new <a href="https://msdn.microsoft.com/CECDE9D5-B5D4-4DF3-80A8-F4B0B37CC5C3">IMFSensorActivitiesReport</a> is available.

</td>
</tr>
</table> 


## -remarks



Register the callback by passing an implementation of this interface into <a href="https://msdn.microsoft.com/852395EE-AA84-4C61-A55F-E8D925FA1447">MFCreateSensorActivityMonitor</a>.



