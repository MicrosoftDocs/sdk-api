---
UID: NN:mbnapi.IMbnDeviceServicesContext
title: IMbnDeviceServicesContext
author: windows-sdk-content
description: Allows for enumerating and retrieving Mobile Broadband device objects on the system.
old-location: mbn\imbndeviceservicescontext.htm
old-project: mbn
ms.assetid: 0B97FCCD-0A90-4FA2-9122-B00BD3F1A033
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMbnDeviceServicesContext, IMbnDeviceServicesContext interface [Microsoft Broadband Networks], IMbnDeviceServicesContext interface [Microsoft Broadband Networks],described, mbn.imbndeviceservicescontext, mbnapi/IMbnDeviceServicesContext
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
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnDeviceServicesContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnDeviceServicesContext interface


## -description


Allows for enumerating and retrieving Mobile Broadband device objects on the system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnDeviceServicesContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnDeviceServicesContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90CB9B2E-16CA-48A0-AF16-937D816718D6">EnumerateDeviceServices</a>
</td>
<td align="left" width="63%">
Gets the list of supported device services by the Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293E9BE5-AD7D-41B7-9A27-E964EE745183">GetDeviceService</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/library/Hh780509(v=VS.85).aspx">IMbnDeviceService</a> object that can be used for communicating with a device service on the Mobile Broadband device.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceServicesContext</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/FCCE3CA1-ECD2-4964-952F-D4A077959519">MaxCommandSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length, in bytes, of data that can be associated with a device service <b>SET</b> or <b>QUERY</b> command.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/E6E29974-083D-4EC8-A4FF-5AACE7435444">MaxDataSize</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The maximum length, in bytes, of data that can be written to or read from a device service session.

</td>
</tr>
</table> 


## -remarks



<b>IMbnDeviceServicesContext</b> objects are provided by a call to the <a href="https://msdn.microsoft.com/20AD207B-6FC3-4493-81F7-41619CA703DB">GetDeviceServicesContext</a> method of the <a href="https://msdn.microsoft.com/6CFF2275-0649-4009-84F2-0657B2FF281C">IMbnDeviceServicesManager</a> interface.



