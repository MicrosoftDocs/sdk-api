---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _L2_NOTIFICATION_DATA structure


## -description


<div class="alert"><b>Important</b>  The <a href="https://msdn.microsoft.com/library/windows/hardware/ff560689">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="netvista.wifi_universal_driver_model">WLAN Universal Windows driver model</a>.</div><div> </div>The L2_NOTIFICATION_DATA structure is used by the IHV Extensions DLL to send notifications to any
  service or applications that has registered for the notification.


## -struct-fields




### -field NotificationSource

This member specifies where the notification comes from. The IHV Extensions DLL must set this
     member to L2_NOTIFICATION_SOURCE_WLAN_IHV.


### -field NotificationCode

This member specifies the notification code for the status indication. This notification code must not have the bit 0x10000 set.


### -field InterfaceGuid

The globally unique identifier (GUID) for the wireless LAN (WLAN) adapter. 
     

The operating system passes the GUID and other data related to the WLAN adapter through the 
     <i>pDot11Adapter</i> parameter of the 
     <a href="https://msdn.microsoft.com/96dc1718-ee35-440a-94e8-eba4a41c9559">
     Dot11ExtIhvInitAdapter</a> function, which the operating system calls when it detects the arrival of
     the WLAN adapter. For more information about this operation, see 
     <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff557044">802.11 WLAN Adapter
     Arrival</a>.


### -field dwDataSize

The length, in bytes, of the data within the buffer referenced by the 
     <b>pData</b> member. The IHV Extensions DLL must set this member to zero if additional data is not
     required for the notification.


### -field pData.unique

 


### -field pData.size_is

 


### -field pData.size_is.dwDataSize

 


### -field pData

The address of a caller-allocated buffer that contains additional data for the notification. The
     format of the data is defined by the independent hardware vendor (IHV).
     

The IHV Extensions DLL must set this member to <b>NULL</b> if additional data is not required for the
     notification.


## -remarks



The application or service registers to receive notifications by calling the 
    <b>WlanRegisterNotification</b> Auto Configuration Manager (ACM) function. For more information about this
    function, refer to the Microsoft Windows SDK documentation.

The IHV Extensions DLL sends notifications to registered services or applications by calling the 
    <a href="https://msdn.microsoft.com/8191b375-537e-44df-920e-077c77ed2354">
    Dot11ExtSendNotification</a> function. The service or application must register to receive
    notifications from a source of L2_NOTIFICATION_SOURCE_WLAN_IHV.




## -see-also




<a href="https://msdn.microsoft.com/96dc1718-ee35-440a-94e8-eba4a41c9559">Dot11ExtIhvInitAdapter</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff547560">Dot11ExtSendNotification</a>
 

 

