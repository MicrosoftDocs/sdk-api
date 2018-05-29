---
UID: NN:mswmdm.IMDSPDevice3
title: IMDSPDevice3
author: windows-sdk-content
description: The IMDSPDevice3 interface must be supported for devices that expect to synchronize with Windows Media Player.
old-location: wmdm\imdspdevice3.htm
old-project: WMDM
ms.assetid: 919c26f4-6954-462a-8b4a-530e78bb72e6
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMDSPDevice3, IMDSPDevice3 interface [windows Media Device Manager], IMDSPDevice3 interface [windows Media Device Manager],described, IMDSPDevice3Interface, mswmdm/IMDSPDevice3, wmdm.imdspdevice3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IMDSPDevice3
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDevice3 interface


## -description



The <b>IMDSPDevice3</b> interface must be supported for devices that expect to synchronize with Windows Media Player. For more information, see <a href="https://msdn.microsoft.com/a312dfef-ac48-4c58-a59a-b277f5386419">Enabling Synchronization with Windows Media Player</a>.

The <b>IMDSPDevice3</b> interface extends <a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2</a> by providing ability to query properties and capabilities of the device with regard to an object format.

<div class="alert"><b>Note</b>  Unless the service provider has added the device parameter <i>UseExtendedWmdm</i> with a value of 1, Windows Media Device Manager will not call this interface. See <a href="https://msdn.microsoft.com/d8774c85-b5c0-4d9e-8a8e-d60ffdf59549">Device Parameters</a> for more information about this.</div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDevice3</b> interface inherits from <a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2</a>. <b>IMDSPDevice3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPDevice3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f41c3f9-8eb6-4d51-87f9-c8b035a73cce">DeviceIoControl</a>
</td>
<td align="left" width="63%">
Calls the device I/O control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/481e6c2d-4103-4818-9ad4-733629af9f9d">FindStorage</a>
</td>
<td align="left" width="63%">
Finds the storage through its unique identification (ID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef53d7d2-dd9c-4705-9a25-9c0b16d03e7e">GetFormatCapability</a>
</td>
<td align="left" width="63%">
Retrieves information from a device about the values or ranges of values supported by the device for each aspect of a particular object format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0665ba6-361d-488c-9100-68f39855b736">GetProperty</a>
</td>
<td align="left" width="63%">
Retrieves device-specific properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72bbf8c3-a7e1-4289-b5b0-a57f50d6f46e">SetProperty</a>
</td>
<td align="left" width="63%">
Sets device-specific properties that are writeable.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice Interface</a>



<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

