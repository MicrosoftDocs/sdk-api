---
UID: NN:mswmdm.IWMDMNotification
title: IWMDMNotification
author: windows-sdk-content
description: The optional, application-implemented IWMDMNotification interface allows applications and service providers to receive notifications when either devices or memory storages (such as RAM cards) are connected or disconnected from the computer.Note  This method will be called only for registered Plug and Play devices. Other device arrivals or departures will not cause this interface to be called. This interface GUID is not properly defined in mssachlp.lib; therefore, you must #include both mswmdm.h and mswmdm_i.c (from wmdm.idl) if implementing this interface, to get the proper definitions.
old-location: wmdm\iwmdmnotification.htm
old-project: WMDM
ms.assetid: 3089a04d-24f5-4a4c-9df5-b4073fef358a
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMNotification, IWMDMNotification interface [windows Media Device Manager], IWMDMNotification interface [windows Media Device Manager],described, IWMDMNotificationInterface, mswmdm/IWMDMNotification, wmdm.iwmdmnotification
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMNotification
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMNotification interface


## -description



The optional, application-implemented <b>IWMDMNotification</b> interface allows applications and service providers to receive notifications when either devices or memory storages (such as RAM cards) are connected or disconnected from the computer.

<div class="alert"><b>Note</b>  This method will be called only for registered Plug and Play devices. Other device arrivals or departures will not cause this interface to be called.</div>
<div> </div>
This interface GUID is not properly defined in mssachlp.lib; therefore, you must #include both mswmdm.h and mswmdm_i.c (from wmdm.idl) if implementing this interface, to get the proper definitions.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMNotification</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMNotification</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMNotification</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e178db6b-2493-442e-95d1-04609b7726fe">WMDMMessage</a>
</td>
<td align="left" width="63%">
Called by Windows Media Device Manager when a device or storage medium is connected or removed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b4fc7714-a7d0-409f-a47c-4903bab883cc">Enabling Notifications</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

