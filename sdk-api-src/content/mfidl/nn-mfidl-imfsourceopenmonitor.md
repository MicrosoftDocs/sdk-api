---
UID: NN:mfidl.IMFSourceOpenMonitor
title: IMFSourceOpenMonitor
author: windows-sdk-content
description: Callback interface to receive notifications from a network source on the progress of an asynchronous open operation.
old-location: mf\imfsourceopenmonitor.htm
old-project: medfound
ms.assetid: 9145910b-81f1-4fd1-8f6f-d6273e0edde6
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: 9145910b-81f1-4fd1-8f6f-d6273e0edde6, IMFSourceOpenMonitor, IMFSourceOpenMonitor interface [Media Foundation], IMFSourceOpenMonitor interface [Media Foundation],described, mf.imfsourceopenmonitor, mfidl/IMFSourceOpenMonitor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceOpenMonitor
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfsensorgroup.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFSourceOpenMonitor interface


## -description


Callback interface to receive notifications from a network source on the progress of an asynchronous open operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceOpenMonitor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSourceOpenMonitor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceOpenMonitor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19b9a891-5116-41b3-8750-85f2c23d3d7f">OnSourceEvent</a>
</td>
<td align="left" width="63%">
Called by the network source when the open operation begins or ends.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/46869f52-323c-41ec-95f7-e7e5d177b782">How to Get Events from the Network Source</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

