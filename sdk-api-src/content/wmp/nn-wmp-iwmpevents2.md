---
UID: NN:wmp.IWMPEvents2
title: IWMPEvents2 (wmp.h)
description: The IWMPEvents2 interface provides events originating from the Windows Media Player 10 or later control to which an embedding program can respond. The events exposed by IWMPEvents2 are also exposed by the _WMPOCXEvents interface.
helpviewer_keywords: ["IWMPEvents2","IWMPEvents2 interface [Windows Media Player]","IWMPEvents2 interface [Windows Media Player]","described","IWMPEvents2Interface","wmp.iwmpevents2_interface","wmp/IWMPEvents2"]
old-location: wmp\iwmpevents2_interface.htm
tech.root: WMP
ms.assetid: 61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d
ms.date: 12/05/2018
ms.keywords: IWMPEvents2, IWMPEvents2 interface [Windows Media Player], IWMPEvents2 interface [Windows Media Player],described, IWMPEvents2Interface, wmp.iwmpevents2_interface, wmp/IWMPEvents2
f1_keywords:
- wmp/IWMPEvents2
dev_langs:
- c++
req.header: wmp.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmp.h
api_name:
- IWMPEvents2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPEvents2 interface


## -description



The <b>IWMPEvents2</b> interface provides events originating from the Windows Media Player 10 or later control to which an embedding program can respond. The events exposed by <b>IWMPEvents2</b> are also exposed by the <b>_WMPOCXEvents</b> interface.



The events provided by <b>IWMPEvents2</b> are related to device synchronization. To receive these events you must create a remoted instance of the Windows Media Player 10 or later control.

In addition to the methods inherited from <b>IWMPEvents</b>, the <b>IWMPEvents2</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-createpartnershipcomplete">CreatePartnershipComplete</a>
</td>
<td>Occurs when an asynchronous call to <b>IWMPSyncDevice::createPartnership</b> completes.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-deviceconnect">DeviceConnect</a>
</td>
<td>Occurs when the user connects a device to the computer.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicedisconnect">DeviceDisconnect</a>
</td>
<td>Occurs when the user disconnects a device from the computer.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicestatuschange">DeviceStatusChange</a>
</td>
<td>Occurs when the partnership status of a device changes.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicesyncerror">DeviceSyncError</a>
</td>
<td>Occurs when a synchronization error happens.</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicesyncstatechange">DeviceSyncStateChange</a>
</td>
<td>Occurs when the synchronization state of a device changes.</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMP/handling-events-in-c">Handling Events in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership">IWMPSyncDevice::createPartnership</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 

