---
UID: NF:mswmdm.IWMDMNotification.WMDMMessage
title: IWMDMNotification::WMDMMessage (mswmdm.h)
description: The WMDMMessage method is a callback method implemented by a client, and called by Windows Media Device Manager when a Plug and Play compliant device or storage medium is connected or removed.
helpviewer_keywords: ["IWMDMNotification interface [windows Media Device Manager]","WMDMMessage method","IWMDMNotification.WMDMMessage","IWMDMNotification::WMDMMessage","IWMDMNotificationWMDMMessage","WMDMMessage","WMDMMessage method [windows Media Device Manager]","WMDMMessage method [windows Media Device Manager]","IWMDMNotification interface","mswmdm/IWMDMNotification::WMDMMessage","wmdm.iwmdmnotification_wmdmmessage"]
old-location: wmdm\iwmdmnotification_wmdmmessage.htm
tech.root: WMDM
ms.assetid: e178db6b-2493-442e-95d1-04609b7726fe
ms.date: 12/05/2018
ms.keywords: IWMDMNotification interface [windows Media Device Manager],WMDMMessage method, IWMDMNotification.WMDMMessage, IWMDMNotification::WMDMMessage, IWMDMNotificationWMDMMessage, WMDMMessage, WMDMMessage method [windows Media Device Manager], WMDMMessage method [windows Media Device Manager],IWMDMNotification interface, mswmdm/IWMDMNotification::WMDMMessage, wmdm.iwmdmnotification_wmdmmessage
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDMNotification::WMDMMessage
 - mswmdm/IWMDMNotification::WMDMMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMNotification.WMDMMessage
---

# IWMDMNotification::WMDMMessage


## -description

The <b>WMDMMessage</b> method is a callback method implemented by a client, and called by Windows Media Device Manager when a Plug and Play compliant device or storage medium is connected or removed.

## -parameters

### -param dwMessageType [in]

A <b>DWORD</b> specifying the message type.

The possible values for the event types are the following:

<table>
<tr>
<th>Message type
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_MSG_DEVICE_ARRIVAL</td>
<td>A device has been connected.</td>
</tr>
<tr>
<td>WMDM_MSG_DEVICE_REMOVAL</td>
<td>A device has been removed.</td>
</tr>
<tr>
<td>WMDM_MSG_MEDIA_ARRIVAL</td>
<td>A storage medium has been inserted in a connected device.</td>
</tr>
<tr>
<td>WMDM_MSG_MEDIA_REMOVAL</td>
<td>A storage medium has been removed from a connected device.</td>
</tr>
</table>

### -param pwszCanonicalName [in]

Pointer to a wide-character, null-terminated string specifying the canonical name of the device for which this event is generated. The application does not release this value.

## -returns

The return value is an <b>HRESULT</b> in which application can return results of its processing of the message. The return value is ignored by WMDM.

## -remarks

To learn how an application subscribes to receive notifications through this method, see <a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>.


#### Examples

The following C++ code implements the <b>WMDMMessage</b> method, and prints out a device or storage arrival or departure notification message.


```cpp

HRESULT WMDMMessage(DWORD  dwMessageType, LPCWSTR  pwszCanonicalName)
{
    switch(dwMessageType)
    {
    case WMDM_MSG_DEVICE_ARRIVAL:
        // TODO: Display a message indicating that a new device has been detected and display the device name.
        break;
    case WMDM_MSG_DEVICE_REMOVAL:
        // TODO: Display a message that the device has been removed and display the device name.
        break;
    case WMDM_MSG_MEDIA_ARRIVAL:
        // TODO: Display a message indicating that storage media has been added to the device and display the device name.
        break;
    case WMDM_MSG_MEDIA_REMOVAL:
        // TODO: Display a message that storage media has been removed from the device and display the device name.
        break;
    default:
        // TODO: Display a message indicating that an unidentified message has been received.
        break;
    }
    return S_OK; // Return value is ignored, and not returned to the application.
}

```

## -see-also

<a href="/windows/desktop/WMDM/enabling-notifications">Enabling Notifications</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification">IWMDMNotification Interface</a>