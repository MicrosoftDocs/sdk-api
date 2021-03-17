---
UID: NF:mmdeviceapi.IMMNotificationClient.OnPropertyValueChanged
title: IMMNotificationClient::OnPropertyValueChanged (mmdeviceapi.h)
description: The OnPropertyValueChanged method indicates that the value of a property belonging to an audio endpoint device has changed.
helpviewer_keywords: ["IMMNotificationClient interface [Core Audio]","OnPropertyValueChanged method","IMMNotificationClient.OnPropertyValueChanged","IMMNotificationClient::OnPropertyValueChanged","IMMNotificationClientOnPropertyValueChanged","OnPropertyValueChanged","OnPropertyValueChanged method [Core Audio]","OnPropertyValueChanged method [Core Audio]","IMMNotificationClient interface","coreaudio.immnotificationclient_onpropertyvaluechanged","mmdeviceapi/IMMNotificationClient::OnPropertyValueChanged"]
old-location: coreaudio\immnotificationclient_onpropertyvaluechanged.htm
tech.root: CoreAudio
ms.assetid: 194aa7d1-4885-49c4-b9c3-2c47468c139f
ms.date: 12/05/2018
ms.keywords: IMMNotificationClient interface [Core Audio],OnPropertyValueChanged method, IMMNotificationClient.OnPropertyValueChanged, IMMNotificationClient::OnPropertyValueChanged, IMMNotificationClientOnPropertyValueChanged, OnPropertyValueChanged, OnPropertyValueChanged method [Core Audio], OnPropertyValueChanged method [Core Audio],IMMNotificationClient interface, coreaudio.immnotificationclient_onpropertyvaluechanged, mmdeviceapi/IMMNotificationClient::OnPropertyValueChanged
req.header: mmdeviceapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMMNotificationClient::OnPropertyValueChanged
 - mmdeviceapi/IMMNotificationClient::OnPropertyValueChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMNotificationClient.OnPropertyValueChanged
---

# IMMNotificationClient::OnPropertyValueChanged


## -description

The <b>OnPropertyValueChanged</b> method indicates that the value of a property belonging to an audio endpoint device has changed.

## -parameters

### -param pwstrDeviceId [in]

Pointer to the <a href="/windows/desktop/CoreAudio/endpoint-id-strings">endpoint ID string</a> that identifies the audio endpoint device. This parameter points to a null-terminated, wide-character string that contains the endpoint ID. The string remains valid for the duration of the call.

### -param key [in]

A <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that specifies the property. The structure contains the property-set GUID and an index identifying a property within the set. The structure is passed by value. It remains valid for the duration of the call. For more information about <b>PROPERTYKEY</b>, see the Windows SDK documentation.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

A call to the <a href="/previous-versions/windows/desktop/legacy/bb761475(v=vs.85)">IPropertyStore::SetValue</a> method that successfully changes the value of a property of an audio endpoint device generates a call to <b>OnPropertyValueChanged</b>. For more information about <b>IPropertyStore::SetValue</b>, see the Windows SDK documentation.

A client can use the <i>key</i> parameter to retrieve the new property value. For a code example that uses a property key to retrieve a property value from the property store of an endpoint device, see <a href="/windows/desktop/CoreAudio/device-properties">Device Properties</a>.

For a code example that implements the <b>OnPropertyValueChanged</b> method, see <a href="/windows/desktop/CoreAudio/device-events">Device Events</a>.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immnotificationclient">IMMNotificationClient Interface</a>