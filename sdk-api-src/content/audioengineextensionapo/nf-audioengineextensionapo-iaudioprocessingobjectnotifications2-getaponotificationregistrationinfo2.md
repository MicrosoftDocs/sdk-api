---
UID: NF:audioengineextensionapo.IAudioProcessingObjectNotifications2.GetApoNotificationRegistrationInfo2
tech.root: audio
title: IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2
ms.date: 02/28/2023
targetos: Windows
description: Called by the system to allow clients to register to receive notification callbacks for APO endpoint and system effect notifications. This method adds a parameter that can be used to determine the notifications types supported on the version of Windows running on the current device.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 22621
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2
f1_keywords:
 - IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2
 - audioengineextensionapo/IAudioProcessingObjectNotifications2::GetApoNotificationRegistrationInfo2
dev_langs:
 - c++
helpviewer_keywords:
 - GetApoNotificationRegistrationInfo2
---

## -description

Called by the system to allow clients to register to receive notification callbacks for APO endpoint and system effect notifications. This method behaves the same as [IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo](./nf-audioengineextensionapo-iaudioprocessingobjectnotifications-getaponotificationregistrationinfo.md) with the addition of a parameter that can be used to determine the notifications types supported on the version of Windows running on the current device.

## -parameters

### -param maxApoNotificationTypeSupported

A value from the [APO_NOTIFICATION_TYPE](./ne-audioengineextensionapo-apo_notification_type.md) enumeration indicating the highest enumeration value supported on the version of Windows running on the current device. Clients can use a comparison operator to determine if a particular notification type is supported.

### -param apoNotifications [out]

Output parameter that returns a pointer to an array of [APO_NOTIFICATION_DESCRIPTOR](ns-audioengineextensionapo-apo_notification_descriptor.md) specifying the set of APO changes for which notifications are requested.

### -param count [out]

Output parameter specifying the number of items returned in *apoNotifications*.

## -returns

An HRESULT.

## -remarks

The following example illustrates a typical implementation of **GetAppNotificationRegistrationInfo2**. The example checks the value of the *maxApoNotificationTypeSupported* parameter to determine if the notifications it is interested in are supported on the version of Windows running on the current device. and, if so, registers for these notifications. 

```cpp
STDMETHODIMP SampleApo::GetApoNotificationRegistrationInfo2(
    UINT32 maxApoNotificationTypeSupported,
    APO_NOTIFICATION_DESCRIPTOR** apoNotificationDescriptorsReturned,
    DWORD* count)
{

    *apoNotificationDescriptorsReturned = nullptr;
    
    *count = 0;
    
    // Before this function can be called, our m_device member variable should already have been initialized.
    // This would typically be done in our implementation of IAudioProcessingObject::Initialize, by using
    // APOInitSystemEffects3::pDeviceCollection to obtain the last IMMDevice in the collection.
    
    RETURN_HR_IF_NULL(E_FAIL, m_device);
    
    if(maxApoNotificationTypeSupported >= APO_NOTIFICATION_TYPE_MICROPHONE_BOOST)
    {
    
        // Let the OS know what notifications we are interested in by returning an array of
        // APO_NOTIFICATION_DESCRIPTORs.
        constexpr DWORD numDescriptors = 3;
        wil::unique_cotaskmem_ptr<APO_NOTIFICATION_DESCRIPTOR[]> apoNotificationDescriptors;
        apoNotificationDescriptors.reset(static_cast<APO_NOTIFICATION_DESCRIPTOR*>(
        CoTaskMemAlloc(sizeof(APO_NOTIFICATION_DESCRIPTOR) * numDescriptors)));
        RETURN_IF_NULL_ALLOC(apoNotificationDescriptors);
        
        // Our APO wants to get notified when the volume level changes on the audio endpoint.
        // The APO_NOTIFICATION_DESCRIPTOR::audioEndpointVolume element is used to specify the audio
        // endpoint for both the APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME and the
        // APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2 notifications.
        apoNotificationDescriptors[0].type = APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2;
        (void)m_device.query_to(&apoNotificationDescriptors[0].audioEndpointVolume.device);
        
        // Our APO also wants to get notified when the orientation of the device changes.
        apoNotificationDescriptors[1].type = APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION;
        
        // Our APO also wants to get notified when the microphone boost changes on the audio endpoint.
        apoNotificationDescriptors[2].type = APO_NOTIFICATION_TYPE_MICROPHONE_BOOST;
        (void)m_device.query_to(&apoNotificationDescriptors[2].audioMicrophoneBoost.device);
        
        // The OS will immediately fire a notification for the above notification types, so we do not
        // need to query the OS for the current values.
        
        *apoNotificationDescriptorsReturned = apoNotificationDescriptors.release();
        *count = numDescriptors;
    
    }
    else
    {
        // If we get here, the APO is running on an older version of Windows that does not support the
        // APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2, APO_NOTIFICATION_TYPE_DEVICE_ORIENTATION, and
        // APO_NOTIFICATION_TYPE_MICROPHONE_BOOST notifications. What the APO does at this point is
        // implementation-specific. For example, the APO may choose to subscribe to the
        // APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME notification instead of
        // APO_NOTIFICATION_TYPE_ENDPOINT_VOLUME2.
    }
    
    return S_OK;

}
```

On windows versions prior to 22621, Windows will only call **IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo**, and not the method on **IAudioProcessingObjectNotifications2**. Since the highest supported notification type on windows versions prior to 22621 was **APO_NOTIFICATION_TYPE_SYSTEM_EFFECTS_PROPERTY_CHANGE**, an APO that needs to run on versions 22621 and older, can choose to simplify their code by using the following implementation for **IAudioProcessingObjectNotifications::GetApoNotificationRegistrationInfo**.


```cpp
STDMETHODIMP SampleApo::GetApoNotificationRegistrationInfo(
    APO_NOTIFICATION_DESCRIPTOR** apoNotificationDescriptorsReturned,
    DWORD* count)
{
    // When the OS invokes GetApoNotificationRegistrationInfo, it implies that the maximum notification value
    // that is supported is APO_NOTIFICATION_TYPE_SYSTEM_EFFECTS_PROPERTY_CHANGE.
    GetApoNotificationRegistrationInfo2(APO_NOTIFICATION_TYPE_SYSTEM_EFFECTS_PROPERTY_CHANGE, apoNotificationDescriptorsReturned, count);
    
    return S_OK;
}
```

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

