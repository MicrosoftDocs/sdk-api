---
UID: NN:mbnapi.IMbnDeviceServicesManager
title: IMbnDeviceServicesManager
author: windows-sdk-content
description: Provides access to IMbnDeviceServicesContext objects and Mobile Broadband device service notifications.
old-location: mbn\imbndeviceservicesmanager.htm
tech.root: mbn
ms.assetid: 6CFF2275-0649-4009-84F2-0657B2FF281C
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IMbnDeviceServicesManager, IMbnDeviceServicesManager interface [Microsoft Broadband Networks], IMbnDeviceServicesManager interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicesmanager, mbnapi/IMbnDeviceServicesManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnDeviceServicesManager interface


## -description


Provides access to <a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a> objects and Mobile Broadband device service notifications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnDeviceServicesManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnDeviceServicesManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20AD207B-6FC3-4493-81F7-41619CA703DB">GetDeviceServicesContext</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a> interface for a specific Mobile Broadband device

</td>
</tr>
</table> 


## -remarks



The following procedure describes how to register for notifications.<ol>
<li>Get an <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a> interface by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on an <b>IMbnDeviceServicesManager</b> object.</li>
<li>Call <a href="https://msdn.microsoft.com/bbe55013-13ca-43e8-8d5e-ef89076df039">FindConnectionPoint</a> on the returned interface and pass IID_IMbnDeviceServicesEvents to RIID.</li>
<li>Call <a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">Advise</a> on the returned connection point and pass a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface on an object that implements <a href="https://msdn.microsoft.com/66A388D0-C704-45D2-AD56-4F81E1928774">IMbnDeviceServicesEvents</a> to PUNK.</li>
</ol>


Notifications can be terminated by calling <a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">Unadvise</a> on the connection point returned in step 2.

For sample code that registers COM notifications, see the Client section of the <a href="http://msdn.microsoft.com/en-us/magazine/cc163361.aspx">COM Connection Points article</a>.



