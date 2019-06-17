---
UID: NF:mfidl.IMFSensorActivityMonitor.Start
title: IMFSensorActivityMonitor::Start (mfidl.h)
author: windows-sdk-content
description: Starts the sensor activity monitor.
old-location: mf\imfsensoractivitymonitor_start.htm
tech.root: medfound
ms.assetid: 49300C9F-CA0B-4515-81C7-02F067B2BBD3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSensorActivityMonitor interface [Media Foundation],Start method, IMFSensorActivityMonitor.Start, IMFSensorActivityMonitor::Start, Start, Start method [Media Foundation], Start method [Media Foundation],IMFSensorActivityMonitor interface, mf.imfsensoractivitymonitor_start, mfidl/IMFSensorActivityMonitor::Start
ms.topic: method
f1_keywords: ["mfidl/IMFSensorActivityMonitor.Start"]
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
 - IMFSensorActivityMonitor.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorActivityMonitor::Start


## -description


Starts the sensor activity monitor.


## -parameters






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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The sensor activity monitor has already been started.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor">IMFSensorActivityMonitor</a>
 

 

