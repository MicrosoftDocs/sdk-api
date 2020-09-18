---
UID: NS:l2cmn._L2_NOTIFICATION_DATA
title: L2_NOTIFICATION_DATA (l2cmn.h)
description: Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later.
helpviewer_keywords: ["*PL2_NOTIFICATION_DATA","L2_NOTIFICATION_DATA","L2_NOTIFICATION_DATA structure [Network Drivers Starting with Windows Vista]","Native_802.11_data_types_56767c07-0bb6-4050-9c44-ed5fd4055ec2.xml","PL2_NOTIFICATION_DATA","PL2_NOTIFICATION_DATA structure pointer [Network Drivers Starting with Windows Vista]","l2cmn/L2_NOTIFICATION_DATA","l2cmn/PL2_NOTIFICATION_DATA","netvista.l2_notification_data"]
old-location: netvista\l2_notification_data.htm
tech.root: NetVista
ms.assetid: 4b67b6c0-2b73-4816-8e85-d6b00227a33c
ms.date: 12/05/2018
ms.keywords: '*PL2_NOTIFICATION_DATA, L2_NOTIFICATION_DATA, L2_NOTIFICATION_DATA structure [Network Drivers Starting with Windows Vista], Native_802.11_data_types_56767c07-0bb6-4050-9c44-ed5fd4055ec2.xml, PL2_NOTIFICATION_DATA, PL2_NOTIFICATION_DATA structure pointer [Network Drivers Starting with Windows Vista], l2cmn/L2_NOTIFICATION_DATA, l2cmn/PL2_NOTIFICATION_DATA, netvista.l2_notification_data'
req.header: l2cmn.h
req.include-header: Wlanihv.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
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
targetos: Windows
req.typenames: L2_NOTIFICATION_DATA, *PL2_NOTIFICATION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _L2_NOTIFICATION_DATA
 - l2cmn/_L2_NOTIFICATION_DATA
 - PL2_NOTIFICATION_DATA
 - l2cmn/PL2_NOTIFICATION_DATA
 - L2_NOTIFICATION_DATA
 - l2cmn/L2_NOTIFICATION_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - l2cmn.h
api_name:
 - L2_NOTIFICATION_DATA
---

# L2_NOTIFICATION_DATA structure


## -description

<div class="alert"><b>Important</b>  The <a href="/windows-hardware/drivers/network/native-802-11-wireless-lan4">Native 802.11 Wireless LAN</a> interface is deprecated in Windows 10 and later. Please use the WLAN Device Driver Interface (WDI) instead. For more information about WDI, see <a href="/windows-hardware/drivers/network/wifi-universal-driver-model">WLAN Universal Windows driver model</a>.</div><div> </div>The L2_NOTIFICATION_DATA structure is used by the IHV Extensions DLL to send notifications to any
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
     <a href="/windows-hardware/drivers/ddi/content/wlanihv/nc-wlanihv-dot11extihv_init_adapter">Dot11ExtIhvInitAdapter</a> function, which the operating system calls when it detects the arrival of
     the WLAN adapter. For more information about this operation, see 
     <a href="/windows/desktop/api/l2cmn/ns-l2cmn-l2_notification_data">802.11 WLAN Adapter
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
    <a href="/windows-hardware/drivers/ddi/content/wlanihv/nc-wlanihv-dot11ext_send_notification">Dot11ExtSendNotification</a> function. The service or application must register to receive
    notifications from a source of L2_NOTIFICATION_SOURCE_WLAN_IHV.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/wlanihv/nc-wlanihv-dot11extihv_init_adapter">Dot11ExtIhvInitAdapter</a>



<a href="/windows-hardware/drivers/ddi/content/wlanihv/nc-wlanihv-dot11ext_send_notification">Dot11ExtSendNotification</a>