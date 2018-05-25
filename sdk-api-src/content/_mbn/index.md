---
UID: TP:mbn
ms.assetid: a50fdfaa-8786-3d51-8479-2ca7260c9904
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Mobile Broadband



Overview of the Mobile Broadband technology.

To develop Mobile Broadband, you need these headers:

 * [mbnapi.h](..\mbnapi\index.md)

For the programming guide, see [Mobile Broadband](/windows/desktop/mbn).

## Structures

| Title   | Description   |
| ---- |:---- |
| [MBN_CONTEXT structure](..\mbnapi\ns-mbnapi-mbn_context.md) | The MBN_CONTEXT structure stores information about the connection context. |
| [MBN_DEVICE_SERVICE structure](..\mbnapi\ns-mbnapi-mbn_device_service.md) | The MBN_DEVICE_SERVICE structure provides information about a Mobile Broadband device service. |
| [MBN_INTERFACE_CAPS structure](..\mbnapi\ns-mbnapi-mbn_interface_caps.md) | The MBN_INTERFACE_CAPS structure represents the interface capabilities. |
| [MBN_PIN_INFO structure](..\mbnapi\ns-mbnapi-mbn_pin_info.md) | The MBN_PIN_INFO structure represents the current PIN state of the device. |
| [MBN_PROVIDER structure](..\mbnapi\ns-mbnapi-mbn_provider.md) | The MBN_PROVIDER structure represents a network service provider. |
| [MBN_PROVIDER2 structure](..\mbnapi\ns-mbnapi-mbn_provider2.md) | The MBN_PROVIDER2 structure represents a network service provider. It is used by many of the provider-specific methods of the IMbnMultiCarrier interface and provides an extension to MBN_PROVIDER to support multi-carrier. |
| [MBN_SMS_FILTER structure](..\mbnapi\ns-mbnapi-mbn_sms_filter.md) | The MBN_SMS_FILTER structure contains the values that describe a set of SMS messages. |
| [MBN_SMS_STATUS_INFO structure](..\mbnapi\ns-mbnapi-mbn_sms_status_info.md) | The MBN_SMS_STATUS_INFO structure contains the status of the SMS message store of a device. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [MBN_ACTIVATION_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_activation_state.md) | The MBN_ACTIVATION_STATE enumerated type indicates the current data connection state. |
| [MBN_AUTH_PROTOCOL enumeration](..\mbnapi\ne-mbnapi-mbn_auth_protocol.md) | The MBN_AUTH_PROTOCOL enumerated type specifies the authentication protocol used for Packet Data Protocol (PDP) activation. |
| [MBN_BAND_CLASS enumeration](..\mbnapi\ne-mbnapi-mbn_band_class.md) | The MBN_BAND_CLASS enumerated type defines the frequency band classes. |
| [MBN_CELLULAR_CLASS enumeration](..\mbnapi\ne-mbnapi-mbn_cellular_class.md) | The MBN_CELLULAR_CLASS enumerated type defines the type of cellular device. |
| [MBN_COMPRESSION enumeration](..\mbnapi\ne-mbnapi-mbn_compression.md) | The MBN_COMPRESSION enumerated type specifies whether compression is to be used in the data link for header and data. |
| [MBN_CONNECTION_MODE enumeration](..\mbnapi\ne-mbnapi-mbn_connection_mode.md) | The MBN_CONNECTION_MODE enumerated type specifies the mode of connection requested. |
| [MBN_CONTEXT_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_context_constants.md) | The MBN_CONTEXT_CONSTANTS enumerated type specifies the maximum string lengths supported by members of the MBN_CONTEXT structure. |
| [MBN_CONTEXT_TYPE enumeration](..\mbnapi\ne-mbnapi-mbn_context_type.md) | The MBN_CONTEXT_TYPE enumerated type specifies the represented context type. |
| [MBN_CTRL_CAPS enumeration](..\mbnapi\ne-mbnapi-mbn_ctrl_caps.md) | The MBN_CTRL_CAPS enumerated type represents all of the Mobile Broadband device control capabilities as bit fields. |
| [MBN_DATA_CLASS enumeration](..\mbnapi\ne-mbnapi-mbn_data_class.md) | The MBN_DATA_CLASS enumerated type specifies the data classes that a provider supports. |
| [MBN_DEVICE_SERVICES_INTERFACE_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_device_services_interface_state.md) | "." |
| [MBN_INTERFACE_CAPS_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_interface_caps_constants.md) | The MBN_INTERFACE_CAPS_CONSTANTS enumerated type defines the maximum length of string values used by assorted elements of the MBN_INTERFACE_CAPS structure. |
| [MBN_MSG_STATUS enumeration](..\mbnapi\ne-mbnapi-mbn_msg_status.md) | The MBN_MSG_STATUS enumerated type defines the type of message being handled. |
| [MBN_PIN_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_pin_constants.md) | The MBN_PIN_CONSTANTS enumerated type defines constant values used by the MBN_PIN_INFO structure. |
| [MBN_PIN_FORMAT enumeration](..\mbnapi\ne-mbnapi-mbn_pin_format.md) | The MBN_PIN_FORMAT enumerated type indicates whether a PIN is numeric or alphanumeric. |
| [MBN_PIN_MODE enumeration](..\mbnapi\ne-mbnapi-mbn_pin_mode.md) | The MBN_PIN_MODE enumerated type indicates if the PIN type is enabled. |
| [MBN_PIN_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_pin_state.md) | The MBN_PIN_STATE enumerated type indicates the current PIN state of the Mobile Broadband device. |
| [MBN_PIN_TYPE enumeration](..\mbnapi\ne-mbnapi-mbn_pin_type.md) | The MBN_PIN_TYPE enumerated type indicates the type of password required for unlocking the information stored on the interface. |
| [MBN_PROVIDER_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_provider_constants.md) | The MBN_PROVIDER_CONSTANTS enumerated type contains values that define the buffer lengths of MBN_PROVIDER members. |
| [MBN_PROVIDER_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_provider_state.md) | The MBN_PROVIDER_STATE enumerated type specifies the various states with which a provider entry can be tagged. |
| [MBN_RADIO enumeration](..\mbnapi\ne-mbnapi-mbn_radio.md) | The MBN_RADIO enumerated type indicates whether the device radio is on or off. |
| [MBN_READY_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_ready_state.md) | The MBN_READY_STATE enumerated type contains values that indicate the readiness of a Mobile Broadband device to engage in cellular network traffic operations. |
| [MBN_REGISTER_MODE enumeration](..\mbnapi\ne-mbnapi-mbn_register_mode.md) | The MBN_REGISTER_MODE enumerated type indicates the network selection mode of a device. |
| [MBN_REGISTER_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_register_state.md) | The MBN_REGISTER_STATE enumerated type indicates the network registration state of a Mobile Broadband device. |
| [MBN_REGISTRATION_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_registration_constants.md) | The MBN_REGISTRATION_CONSTANTS enumerated type contains specific values used by IMbnRegistration interface operations. |
| [MBN_SIGNAL_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_signal_constants.md) | THE MBN_SIGNAL_CONSTANTS enumerated type contains specific values used by IMbnSignal interface operations. |
| [MBN_SMS_CDMA_ENCODING enumeration](..\mbnapi\ne-mbnapi-mbn_sms_cdma_encoding.md) | The MBN_SMS_CDMA_ENCODING enumerated type specifies character encoding types for CDMA. |
| [MBN_SMS_CDMA_LANG enumeration](..\mbnapi\ne-mbnapi-mbn_sms_cdma_lang.md) | The MBN_SMS_CDMA_LANG enumerated type represents the different languages that can be used in a CDMA message. |
| [MBN_SMS_CONSTANTS enumeration](..\mbnapi\ne-mbnapi-mbn_sms_constants.md) | The MBN_SMS_CONSTANTS enumerated type contains SMS constant values. |
| [MBN_SMS_FLAG enumeration](..\mbnapi\ne-mbnapi-mbn_sms_flag.md) | The MBN_SMS_FLAG enumerated type specifies the SMS message class. |
| [MBN_SMS_FORMAT enumeration](..\mbnapi\ne-mbnapi-mbn_sms_format.md) | Format of SMS messages. |
| [MBN_SMS_STATUS_FLAG enumeration](..\mbnapi\ne-mbnapi-mbn_sms_status_flag.md) | The MBN_SMS_STATUS_FLAG enumerated type indicates the status of a device's SMS message store. |
| [MBN_VOICE_CALL_STATE enumeration](..\mbnapi\ne-mbnapi-mbn_voice_call_state.md) | The MBN_VOICE_CALL_STATE enumerated type specifies the current voice call state of the device. |
| [MBN_VOICE_CLASS enumeration](..\mbnapi\ne-mbnapi-mbn_voice_class.md) | The MBN_VOICE_CLASS enumerated type specifies a device's voice capabilities and how they interact with the data service. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IMbnConnection interface](..\mbnapi\nn-mbnapi-imbnconnection.md) | Represents the network connectivity of a device. |
| [IMbnConnectionContext interface](..\mbnapi\nn-mbnapi-imbnconnectioncontext.md) | Manages connection contexts. |
| [IMbnConnectionContextEvents interface](..\mbnapi\nn-mbnapi-imbnconnectioncontextevents.md) | This notification interface is used to handle asynchronous provisioned context events. |
| [IMbnConnectionEvents interface](..\mbnapi\nn-mbnapi-imbnconnectionevents.md) | This notification interface signals an application about change and completion status of asynchronous connection requests. |
| [IMbnConnectionManager interface](..\mbnapi\nn-mbnapi-imbnconnectionmanager.md) | Provides access to IMbnConnection objects and connection notifications. |
| [IMbnConnectionManagerEvents interface](..\mbnapi\nn-mbnapi-imbnconnectionmanagerevents.md) | This notification interface signals an application about the arrival and removal of IMbnConnection interfaces in the system. |
| [IMbnConnectionProfile interface](..\mbnapi\nn-mbnapi-imbnconnectionprofile.md) | This interface accesses connection parameters and preferences stored in Mobile Broadband profiles. |
| [IMbnConnectionProfileEvents interface](..\mbnapi\nn-mbnapi-imbnconnectionprofileevents.md) | This notification interface signals an application when IMbnConnectionProfile methods change the Mobile Broadband profile state. |
| [IMbnConnectionProfileManager interface](..\mbnapi\nn-mbnapi-imbnconnectionprofilemanager.md) | Provides access to connection profiles and connection notifications. |
| [IMbnConnectionProfileManagerEvents interface](..\mbnapi\nn-mbnapi-imbnconnectionprofilemanagerevents.md) | This notification interface signals an application about the arrival and removal of IMbnConnectionProfile interfaces in the system. |
| [IMbnDeviceService interface](..\mbnapi\nn-mbnapi-imbndeviceservice.md) | Allows for communicating with a device service on a particular Mobile Broadband device. |
| [IMbnDeviceServicesContext interface](..\mbnapi\nn-mbnapi-imbndeviceservicescontext.md) | Allows for enumerating and retrieving Mobile Broadband device objects on the system. |
| [IMbnDeviceServicesEvents interface](..\mbnapi\nn-mbnapi-imbndeviceservicesevents.md) | Signals an application about notification events related to Mobile Broadband device services on the system. |
| [IMbnDeviceServicesManager interface](..\mbnapi\nn-mbnapi-imbndeviceservicesmanager.md) | Provides access to IMbnDeviceServicesContext objects and Mobile Broadband device service notifications. |
| [IMbnInterface interface](..\mbnapi\nn-mbnapi-imbninterface.md) | Represents a Mobile Broadband device. |
| [IMbnInterfaceEvents interface](..\mbnapi\nn-mbnapi-imbninterfaceevents.md) | This interface is a notification interface used to handle asynchronous IMbnInterface method calls as well as changes in the device state. |
| [IMbnInterfaceManager interface](..\mbnapi\nn-mbnapi-imbninterfacemanager.md) | Provides access to IMbnInterface objects and notifications. |
| [IMbnInterfaceManagerEvents interface](..\mbnapi\nn-mbnapi-imbninterfacemanagerevents.md) | This notification interface signals an application about the arrival and removal of devices in the system. |
| [IMbnMultiCarrier interface](..\mbnapi\nn-mbnapi-imbnmulticarrier.md) | This interface exposes the multi-carrier functionality of a capable Mobile Broadband device. |
| [IMbnMultiCarrierEvents interface](..\mbnapi\nn-mbnapi-imbnmulticarrierevents.md) | This interface is a notification interface used to handle asynchronous IMbnMultiCarrier method calls. |
| [IMbnPin interface](..\mbnapi\nn-mbnapi-imbnpin.md) | Represents the device PIN. |
| [IMbnPinEvents interface](..\mbnapi\nn-mbnapi-imbnpinevents.md) | This interface is a notification interface used to indicate when asynchronous PIN requests have completed. |
| [IMbnPinManager interface](..\mbnapi\nn-mbnapi-imbnpinmanager.md) | Provides important details about the device PIN. |
| [IMbnPinManagerEvents interface](..\mbnapi\nn-mbnapi-imbnpinmanagerevents.md) | Notification interface used to indicate when PIN Manager events have occurred. |
| [IMbnRadio interface](..\mbnapi\nn-mbnapi-imbnradio.md) | The IMbnRadio interface is used to query and update the radio state of Mobile Broadband devices. |
| [IMbnRadioEvents interface](..\mbnapi\nn-mbnapi-imbnradioevents.md) | Notification interface used to indicate a change in the radio state as well as the completion of a programatic change in the state . |
| [IMbnRegistration interface](..\mbnapi\nn-mbnapi-imbnregistration.md) | Provides access to network registration data. |
| [IMbnRegistrationEvents interface](..\mbnapi\nn-mbnapi-imbnregistrationevents.md) | Notification interface used to indicate when registration events have occurred. |
| [IMbnServiceActivation interface](..\mbnapi\nn-mbnapi-imbnserviceactivation.md) | Pass-through mechanism for cellular service activation. |
| [IMbnServiceActivationEvents interface](..\mbnapi\nn-mbnapi-imbnserviceactivationevents.md) | This notification interface signals an application about the completion of a service activation request. |
| [IMbnSignal interface](..\mbnapi\nn-mbnapi-imbnsignal.md) | Get radio signal quality of a Mobile Broadband connection. |
| [IMbnSignalEvents interface](..\mbnapi\nn-mbnapi-imbnsignalevents.md) | Notification interface used to indicate that a signal event has occurred. |
| [IMbnSms interface](..\mbnapi\nn-mbnapi-imbnsms.md) | SMS interface for sending and receiving messages as well as controlling the messaging configuration. |
| [IMbnSmsConfiguration interface](..\mbnapi\nn-mbnapi-imbnsmsconfiguration.md) | Provides access to the SMS configuration of a device. |
| [IMbnSmsEvents interface](..\mbnapi\nn-mbnapi-imbnsmsevents.md) | This notification interface signals an application with the completion status of SMS operations and changes in the device SMS status. |
| [IMbnSmsReadMsgPdu interface](..\mbnapi\nn-mbnapi-imbnsmsreadmsgpdu.md) | A collection of properties that represent an SMS message read from the device memory. |
| [IMbnSmsReadMsgTextCdma interface](..\mbnapi\nn-mbnapi-imbnsmsreadmsgtextcdma.md) | A collection of properties that represent a CDMA format SMS message read from the device memory. |
| [IMbnSubscriberInformation interface](..\mbnapi\nn-mbnapi-imbnsubscriberinformation.md) | Provides access to subscriber information. |
| [IMbnVendorSpecificEvents interface](..\mbnapi\nn-mbnapi-imbnvendorspecificevents.md) | This notification interface signals an application of the completion status of vendor-specific operations and other vendor-specific changes in the device state. |
| [IMbnVendorSpecificOperation interface](..\mbnapi\nn-mbnapi-imbnvendorspecificoperation.md) | Interface to pass requests from an application to the underlying Mobile Broadband miniport drivers. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IMbnConnection::Connect](..\mbnapi\nf-mbnapi-imbnconnection-connect.md) | Establishes a data connection. |
| [IMbnConnection::Disconnect](..\mbnapi\nf-mbnapi-imbnconnection-disconnect.md) | Disconnects a data connection. |
| [IMbnConnection::GetActivationNetworkError](..\mbnapi\nf-mbnapi-imbnconnection-getactivationnetworkerror.md) | Gets the network error returned in a Packet Data Protocol (PDP) context activation failure. |
| [IMbnConnection::GetConnectionState](..\mbnapi\nf-mbnapi-imbnconnection-getconnectionstate.md) | Gets the current connection state of the device. |
| [IMbnConnection::GetVoiceCallState](..\mbnapi\nf-mbnapi-imbnconnection-getvoicecallstate.md) | Gets the voice call state of the device. |
| [IMbnConnection::get_ConnectionID](..\mbnapi\nf-mbnapi-imbnconnection-get_connectionid.md) | Gets the unique identifier for the connection. |
| [IMbnConnection::get_InterfaceID](..\mbnapi\nf-mbnapi-imbnconnection-get_interfaceid.md) | Gets the interface identifier. |
| [IMbnConnectionContext::GetProvisionedContexts](..\mbnapi\nf-mbnapi-imbnconnectioncontext-getprovisionedcontexts.md) | Gets a list of connection contexts. |
| [IMbnConnectionContext::SetProvisionedContext](..\mbnapi\nf-mbnapi-imbnconnectioncontext-setprovisionedcontext.md) | Adds or updates a provisioned context. |
| [IMbnConnectionContextEvents::OnProvisionedContextListChange](..\mbnapi\nf-mbnapi-imbnconnectioncontextevents-onprovisionedcontextlistchange.md) | Notification method called by the Mobile Broadband service to indicate that a provisioned context stored in the device is available or updated. |
| [IMbnConnectionContextEvents::OnSetProvisionedContextComplete](..\mbnapi\nf-mbnapi-imbnconnectioncontextevents-onsetprovisionedcontextcomplete.md) | Notification method called by the Mobile Broadband service to indicate that the provisioned context in the device has been set. |
| [IMbnConnectionEvents::OnConnectComplete](..\mbnapi\nf-mbnapi-imbnconnectionevents-onconnectcomplete.md) | Notification method that signals the completion of a connection operation. |
| [IMbnConnectionEvents::OnConnectStateChange](..\mbnapi\nf-mbnapi-imbnconnectionevents-onconnectstatechange.md) | Notification method that indicates whether the connection state of the device has changed. |
| [IMbnConnectionEvents::OnDisconnectComplete](..\mbnapi\nf-mbnapi-imbnconnectionevents-ondisconnectcomplete.md) | Notification method that indicates that a disconnection operation has been performed. |
| [IMbnConnectionEvents::OnVoiceCallStateChange](..\mbnapi\nf-mbnapi-imbnconnectionevents-onvoicecallstatechange.md) | Notification method that indicates a change in the voice call state of a device. |
| [IMbnConnectionManager::GetConnection](..\mbnapi\nf-mbnapi-imbnconnectionmanager-getconnection.md) | Gets a connection. |
| [IMbnConnectionManager::GetConnections](..\mbnapi\nf-mbnapi-imbnconnectionmanager-getconnections.md) | Gets a list of available connections. |
| [IMbnConnectionManagerEvents::OnConnectionArrival](..\mbnapi\nf-mbnapi-imbnconnectionmanagerevents-onconnectionarrival.md) | Notification method that indicates a new connection was added to the system. |
| [IMbnConnectionManagerEvents::OnConnectionRemoval](..\mbnapi\nf-mbnapi-imbnconnectionmanagerevents-onconnectionremoval.md) | Notification method that indicates a connection was removed from the system. |
| [IMbnConnectionProfile::Delete](..\mbnapi\nf-mbnapi-imbnconnectionprofile-delete.md) | Deletes the profile from the system. |
| [IMbnConnectionProfile::GetProfileXmlData](..\mbnapi\nf-mbnapi-imbnconnectionprofile-getprofilexmldata.md) | Gets the XML data of the current profile. |
| [IMbnConnectionProfile::UpdateProfile](..\mbnapi\nf-mbnapi-imbnconnectionprofile-updateprofile.md) | Updates the contents of the profile. |
| [IMbnConnectionProfileEvents::OnProfileUpdate](..\mbnapi\nf-mbnapi-imbnconnectionprofileevents-onprofileupdate.md) | A notification method that indicates that profile update operation has completed. |
| [IMbnConnectionProfileManager::CreateConnectionProfile](..\mbnapi\nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile.md) | Creates a new connection profile for the device. |
| [IMbnConnectionProfileManager::GetConnectionProfile](..\mbnapi\nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofile.md) | Gets a specific connection profile associated with the given Mobile Broadband device. |
| [IMbnConnectionProfileManager::GetConnectionProfiles](..\mbnapi\nf-mbnapi-imbnconnectionprofilemanager-getconnectionprofiles.md) | Gets a list of connection profiles associated with the device. |
| [IMbnConnectionProfileManagerEvents::OnConnectionProfileArrival](..\mbnapi\nf-mbnapi-imbnconnectionprofilemanagerevents-onconnectionprofilearrival.md) | Notification method that indicates a new connection profile has been added to the system. |
| [IMbnConnectionProfileManagerEvents::OnConnectionProfileRemoval](..\mbnapi\nf-mbnapi-imbnconnectionprofilemanagerevents-onconnectionprofileremoval.md) | Notification method that indicates a connection profile has been removed from the system. |
| [IMbnDeviceService::CloseCommandSession](..\mbnapi\nf-mbnapi-imbndeviceservice-closecommandsession.md) | Closes a command session to a device service on a Mobile Broadband device. |
| [IMbnDeviceService::CloseDataSession](..\mbnapi\nf-mbnapi-imbndeviceservice-closedatasession.md) | Closes the data session to a device service on a Mobile Broadband device. |
| [IMbnDeviceService::OpenCommandSession](..\mbnapi\nf-mbnapi-imbndeviceservice-opencommandsession.md) | Opens a command session to a device service on a Mobile Broadband device. |
| [IMbnDeviceService::QueryCommand](..\mbnapi\nf-mbnapi-imbndeviceservice-querycommand.md) | Sends a QUERY control command to the device service of a Mobile Broadband device. |
| [IMbnDeviceService::QuerySupportedCommands](..\mbnapi\nf-mbnapi-imbndeviceservice-querysupportedcommands.md) | Gets the list of commands IDs supported by the Mobile Broadband device service. |
| [IMbnDeviceService::SetCommand](..\mbnapi\nf-mbnapi-imbndeviceservice-setcommand.md) | Sends a SET control command to the device service of a Mobile Broadband device. |
| [IMbnDeviceService::get_DeviceServiceID](..\mbnapi\nf-mbnapi-imbndeviceservice-get_deviceserviceid.md) | The ID of the device service to which this object is associated. |
| [IMbnDeviceService::get_IsCommandSessionOpen](..\mbnapi\nf-mbnapi-imbndeviceservice-get_iscommandsessionopen.md) | Reports if the device service command session is open. |
| [IMbnDeviceService::get_IsDataSessionOpen](..\mbnapi\nf-mbnapi-imbndeviceservice-get_isdatasessionopen.md) | Reports if the device service data session is open. |
| [IMbnDeviceServicesContext::EnumerateDeviceServices](..\mbnapi\nf-mbnapi-imbndeviceservicescontext-enumeratedeviceservices.md) | Gets the list of supported device services by the Mobile Broadband device. |
| [IMbnDeviceServicesContext::GetDeviceService](..\mbnapi\nf-mbnapi-imbndeviceservicescontext-getdeviceservice.md) | Gets the IMbnDeviceService object that can be used for communicating with a device service on the Mobile Broadband device. |
| [IMbnDeviceServicesContext::get_MaxCommandSize](..\mbnapi\nf-mbnapi-imbndeviceservicescontext-get_maxcommandsize.md) | The maximum length, in bytes, of data that can be associated with a device service SET or QUERY command. |
| [IMbnDeviceServicesContext::get_MaxDataSize](..\mbnapi\nf-mbnapi-imbndeviceservicescontext-get_maxdatasize.md) | The maximum length, in bytes, of data that can be written to or read from a device service session. |
| [IMbnDeviceServicesEvents::OnCloseCommandSessionComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onclosecommandsessioncomplete.md) | Notification method indicating that a device service CloseCommandSession request has completed. |
| [IMbnDeviceServicesEvents::OnCloseDataSessionComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onclosedatasessioncomplete.md) | Notification method indicating that a device service session CloseDataSession request has completed. |
| [IMbnDeviceServicesEvents::OnEventNotification](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-oneventnotification.md) | Notification method signaling a device service state change event from the Mobile Broadband device. |
| [IMbnDeviceServicesEvents::OnInterfaceStateChange](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-oninterfacestatechange.md) | Notification method that signals a change in the state of device services on the system. |
| [IMbnDeviceServicesEvents::OnOpenCommandSessionComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onopencommandsessioncomplete.md) | Notification method indicating that a device service CommandSessionOpen request has completed. |
| [IMbnDeviceServicesEvents::OnOpenDataSessionComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onopendatasessioncomplete.md) | Notification method indicating that a device service OpenDataSession request has completed. |
| [IMbnDeviceServicesEvents::OnQueryCommandComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onquerycommandcomplete.md) | Notification method indicating that a device service QUERY request has completed. |
| [IMbnDeviceServicesEvents::OnQuerySupportedCommandsComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onquerysupportedcommandscomplete.md) | Notification method indicating that a query for the messages supported on a device service has completed. |
| [IMbnDeviceServicesEvents::OnReadData](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onreaddata.md) | Notification for data being read from a device service data session. |
| [IMbnDeviceServicesEvents::OnSetCommandComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onsetcommandcomplete.md) | Notification method indicating that a device service SET request has completed. |
| [IMbnDeviceServicesEvents::OnWriteDataComplete](..\mbnapi\nf-mbnapi-imbndeviceservicesevents-onwritedatacomplete.md) | Notification method indicating that a device service session Write request has completed. |
| [IMbnDeviceServicesManager::GetDeviceServicesContext](..\mbnapi\nf-mbnapi-imbndeviceservicesmanager-getdeviceservicescontext.md) | Gets the IMbnDeviceServicesContext interface for a specific Mobile Broadband device. |
| [IMbnInterface::GetConnection](..\mbnapi\nf-mbnapi-imbninterface-getconnection.md) | Gets the IMbnConnection object. |
| [IMbnInterface::GetHomeProvider](..\mbnapi\nf-mbnapi-imbninterface-gethomeprovider.md) | Gets the home provider. |
| [IMbnInterface::GetInterfaceCapability](..\mbnapi\nf-mbnapi-imbninterface-getinterfacecapability.md) | Gets the capabilities of the device. |
| [IMbnInterface::GetPreferredProviders](..\mbnapi\nf-mbnapi-imbninterface-getpreferredproviders.md) | Gets the list of preferred providers. |
| [IMbnInterface::GetReadyState](..\mbnapi\nf-mbnapi-imbninterface-getreadystate.md) | Gets the ready state. |
| [IMbnInterface::GetSubscriberInformation](..\mbnapi\nf-mbnapi-imbninterface-getsubscriberinformation.md) | Gets the subscriber information. |
| [IMbnInterface::GetVisibleProviders](..\mbnapi\nf-mbnapi-imbninterface-getvisibleproviders.md) | Gets the list of visible providers. |
| [IMbnInterface::InEmergencyMode](..\mbnapi\nf-mbnapi-imbninterface-inemergencymode.md) | Determines whether the device is in emergency mode. |
| [IMbnInterface::ScanNetwork](..\mbnapi\nf-mbnapi-imbninterface-scannetwork.md) | Asynchronously scans the network to get a list of visible providers. |
| [IMbnInterface::SetPreferredProviders](..\mbnapi\nf-mbnapi-imbninterface-setpreferredproviders.md) | Updates the preferred providers list for the device. |
| [IMbnInterface::get_InterfaceID](..\mbnapi\nf-mbnapi-imbninterface-get_interfaceid.md) | The interface ID. |
| [IMbnInterfaceEvents::OnEmergencyModeChange](..\mbnapi\nf-mbnapi-imbninterfaceevents-onemergencymodechange.md) | This notification method is called by the Mobile Broadband service to indicate that the emergency mode has changed. |
| [IMbnInterfaceEvents::OnHomeProviderAvailable](..\mbnapi\nf-mbnapi-imbninterfaceevents-onhomeprovideravailable.md) | This notification method is called by the Mobile Broadband service to indicate that home provider information for the device is available. |
| [IMbnInterfaceEvents::OnInterfaceCapabilityAvailable](..\mbnapi\nf-mbnapi-imbninterfaceevents-oninterfacecapabilityavailable.md) | This notification method is called by the Mobile Broadband service to indicate that interface capability information is available. |
| [IMbnInterfaceEvents::OnPreferredProvidersChange](..\mbnapi\nf-mbnapi-imbninterfaceevents-onpreferredproviderschange.md) | This notification method is called by the Mobile Broadband service to indicate a change in a device's preferred provider list. |
| [IMbnInterfaceEvents::OnReadyStateChange](..\mbnapi\nf-mbnapi-imbninterfaceevents-onreadystatechange.md) | This notification method is called by the Mobile Broadband service to indicate a change in an interface's ready state. |
| [IMbnInterfaceEvents::OnScanNetworkComplete](..\mbnapi\nf-mbnapi-imbninterfaceevents-onscannetworkcomplete.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a network scan. |
| [IMbnInterfaceEvents::OnSetPreferredProvidersComplete](..\mbnapi\nf-mbnapi-imbninterfaceevents-onsetpreferredproviderscomplete.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a SetPreferredProviders operation. |
| [IMbnInterfaceEvents::OnSubscriberInformationChange](..\mbnapi\nf-mbnapi-imbninterfaceevents-onsubscriberinformationchange.md) | This notification method is called by the Mobile Broadband service to indicate that the subscriber information for the device has changed. |
| [IMbnInterfaceManager::GetInterface](..\mbnapi\nf-mbnapi-imbninterfacemanager-getinterface.md) | Gets a specific interface. |
| [IMbnInterfaceManager::GetInterfaces](..\mbnapi\nf-mbnapi-imbninterfacemanager-getinterfaces.md) | Gets a list of all available IMbnInterface objects. |
| [IMbnInterfaceManagerEvents::OnInterfaceArrival](..\mbnapi\nf-mbnapi-imbninterfacemanagerevents-oninterfacearrival.md) | Notification method that signals that a device has been added to the system. |
| [IMbnInterfaceManagerEvents::OnInterfaceRemoval](..\mbnapi\nf-mbnapi-imbninterfacemanagerevents-oninterfaceremoval.md) | Notification method that signals that a device has been removed from the system. |
| [IMbnMultiCarrier::GetCurrentCellularClass](..\mbnapi\nf-mbnapi-imbnmulticarrier-getcurrentcellularclass.md) | Gets the current cellular classes for a multi-carrier device. |
| [IMbnMultiCarrier::GetPreferredProviders](..\mbnapi\nf-mbnapi-imbnmulticarrier-getpreferredproviders.md) | Gets the list of subscribed providers visible in the current area for a multi-carrier device minus the current registered provider. |
| [IMbnMultiCarrier::GetSupportedCellularClasses](..\mbnapi\nf-mbnapi-imbnmulticarrier-getsupportedcellularclasses.md) | Gets the list of supported cellular classes for a multi-carrier device. |
| [IMbnMultiCarrier::GetVisibleProviders](..\mbnapi\nf-mbnapi-imbnmulticarrier-getvisibleproviders.md) | Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers. |
| [IMbnMultiCarrier::ScanNetwork](..\mbnapi\nf-mbnapi-imbnmulticarrier-scannetwork.md) | Scans the network to get a list of visible providers for a multi-carrier device. |
| [IMbnMultiCarrier::SetHomeProvider](..\mbnapi\nf-mbnapi-imbnmulticarrier-sethomeprovider.md) | Updates the home provider for a multi-carrier device. |
| [IMbnMultiCarrierEvents::OnCurrentCellularClassChange](..\mbnapi\nf-mbnapi-imbnmulticarrierevents-oncurrentcellularclasschange.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a GetCurrentCellularClass operation. |
| [IMbnMultiCarrierEvents::OnInterfaceCapabilityChange](..\mbnapi\nf-mbnapi-imbnmulticarrierevents-oninterfacecapabilitychange.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation that updates the interface capabilities. |
| [IMbnMultiCarrierEvents::OnPreferredProvidersChange](..\mbnapi\nf-mbnapi-imbnmulticarrierevents-onpreferredproviderschange.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a GetPreferredProviders operation and a change in a device's preferred provider list. |
| [IMbnMultiCarrierEvents::OnScanNetworkComplete](..\mbnapi\nf-mbnapi-imbnmulticarrierevents-onscannetworkcomplete.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a ScanNetwork operation. |
| [IMbnMultiCarrierEvents::OnSetHomeProviderComplete](..\mbnapi\nf-mbnapi-imbnmulticarrierevents-onsethomeprovidercomplete.md) | This notification method is called by the Mobile Broadband service to indicate the completion of a SetHomeProvider operation. |
| [IMbnPin::Change](..\mbnapi\nf-mbnapi-imbnpin-change.md) | Changes the PIN. |
| [IMbnPin::Disable](..\mbnapi\nf-mbnapi-imbnpin-disable.md) | Disables a PIN. |
| [IMbnPin::Enable](..\mbnapi\nf-mbnapi-imbnpin-enable.md) | Enables a PIN. |
| [IMbnPin::Enter](..\mbnapi\nf-mbnapi-imbnpin-enter.md) | Enters a PIN. |
| [IMbnPin::GetPinManager](..\mbnapi\nf-mbnapi-imbnpin-getpinmanager.md) | Gets the IMbnPinManager. |
| [IMbnPin::Unblock](..\mbnapi\nf-mbnapi-imbnpin-unblock.md) | Unblocks a blocked PIN. |
| [IMbnPin::get_PinFormat](..\mbnapi\nf-mbnapi-imbnpin-get_pinformat.md) | The PIN format. |
| [IMbnPin::get_PinLengthMax](..\mbnapi\nf-mbnapi-imbnpin-get_pinlengthmax.md) | The maximum length of the PIN. |
| [IMbnPin::get_PinLengthMin](..\mbnapi\nf-mbnapi-imbnpin-get_pinlengthmin.md) | The minimum length of the PIN. |
| [IMbnPin::get_PinMode](..\mbnapi\nf-mbnapi-imbnpin-get_pinmode.md) | The PIN mode. |
| [IMbnPin::get_PinType](..\mbnapi\nf-mbnapi-imbnpin-get_pintype.md) | The PIN type. |
| [IMbnPinEvents::OnChangeComplete](..\mbnapi\nf-mbnapi-imbnpinevents-onchangecomplete.md) | Notification method called by the Mobile Broadband service to indicate that a PIN change operation has completed. |
| [IMbnPinEvents::OnDisableComplete](..\mbnapi\nf-mbnapi-imbnpinevents-ondisablecomplete.md) | Notification method called by the Mobile Broadband service to indicate that a PIN disable operation has completed. |
| [IMbnPinEvents::OnEnableComplete](..\mbnapi\nf-mbnapi-imbnpinevents-onenablecomplete.md) | Notification method called by the Mobile Broadband service to indicate that a PIN enable operation has completed. |
| [IMbnPinEvents::OnEnterComplete](..\mbnapi\nf-mbnapi-imbnpinevents-onentercomplete.md) | Notification method called by the Mobile Broadband service to indicate that a PIN enter operation has completed. |
| [IMbnPinEvents::OnUnblockComplete](..\mbnapi\nf-mbnapi-imbnpinevents-onunblockcomplete.md) | Notification method called by the Mobile Broadband service to indicate that a PIN unblock operation has completed. |
| [IMbnPinManager::GetPinList](..\mbnapi\nf-mbnapi-imbnpinmanager-getpinlist.md) | Gets a list of different PIN types supported by the device. |
| [IMbnPinManager::GetPinState](..\mbnapi\nf-mbnapi-imbnpinmanager-getpinstate.md) | Gets the current PIN state of the device. |
| [IMbnPinManager::GetPin](..\mbnapi\nf-mbnapi-imbnpinmanager-getpin.md) | Gets a specific type of PIN. |
| [IMbnPinManagerEvents::OnGetPinStateComplete](..\mbnapi\nf-mbnapi-imbnpinmanagerevents-ongetpinstatecomplete.md) | Notification method called by the Mobile Broadband service to indicate the completion of an asynchronous operation triggered by a call to the GetPinState method of IMbnPinManager. |
| [IMbnPinManagerEvents::OnPinListAvailable](..\mbnapi\nf-mbnapi-imbnpinmanagerevents-onpinlistavailable.md) | Notification method called by the Mobile Broadband service to indicate that the list of device PINs is available. |
| [IMbnRadio::SetSoftwareRadioState](..\mbnapi\nf-mbnapi-imbnradio-setsoftwareradiostate.md) | Sets the software radio state of a Mobile Broadband device. |
| [IMbnRadio::get_HardwareRadioState](..\mbnapi\nf-mbnapi-imbnradio-get_hardwareradiostate.md) | The hardware radio state of a Mobile Broadband device. |
| [IMbnRadio::get_SoftwareRadioState](..\mbnapi\nf-mbnapi-imbnradio-get_softwareradiostate.md) | The software radio state of a Mobile Broadband device. |
| [IMbnRadioEvents::OnRadioStateChange](..\mbnapi\nf-mbnapi-imbnradioevents-onradiostatechange.md) | A notification signaling that the radio state of the device has changed. |
| [IMbnRadioEvents::OnSetSoftwareRadioStateComplete](..\mbnapi\nf-mbnapi-imbnradioevents-onsetsoftwareradiostatecomplete.md) | Notification that a set software radio state operation has completed. |
| [IMbnRegistration::GetAvailableDataClasses](..\mbnapi\nf-mbnapi-imbnregistration-getavailabledataclasses.md) | Gets the available data classes in the current network. |
| [IMbnRegistration::GetCurrentDataClass](..\mbnapi\nf-mbnapi-imbnregistration-getcurrentdataclass.md) | Gets the current data class in the current network. |
| [IMbnRegistration::GetPacketAttachNetworkError](..\mbnapi\nf-mbnapi-imbnregistration-getpacketattachnetworkerror.md) | Gets the network error from a packet attach operation. |
| [IMbnRegistration::GetProviderID](..\mbnapi\nf-mbnapi-imbnregistration-getproviderid.md) | Gets the provider ID for the currently registered network. |
| [IMbnRegistration::GetProviderName](..\mbnapi\nf-mbnapi-imbnregistration-getprovidername.md) | Gets the provider name for the currently registered network. |
| [IMbnRegistration::GetRegisterMode](..\mbnapi\nf-mbnapi-imbnregistration-getregistermode.md) | Gets the network registration mode of a Mobile Broadband device. |
| [IMbnRegistration::GetRegisterState](..\mbnapi\nf-mbnapi-imbnregistration-getregisterstate.md) | Gets the registration state. |
| [IMbnRegistration::GetRegistrationNetworkError](..\mbnapi\nf-mbnapi-imbnregistration-getregistrationnetworkerror.md) | Gets the network error from a registration operation. |
| [IMbnRegistration::GetRoamingText](..\mbnapi\nf-mbnapi-imbnregistration-getroamingtext.md) | Gets the roaming text describing the roaming provider. |
| [IMbnRegistration::SetRegisterMode](..\mbnapi\nf-mbnapi-imbnregistration-setregistermode.md) | Sets the registration mode for the device. |
| [IMbnRegistrationEvents::OnPacketServiceStateChange](..\mbnapi\nf-mbnapi-imbnregistrationevents-onpacketservicestatechange.md) | Notification method called by the Mobile Broadband service to indicate a change in the device packet service state. |
| [IMbnRegistrationEvents::OnRegisterModeAvailable](..\mbnapi\nf-mbnapi-imbnregistrationevents-onregistermodeavailable.md) | Notification method called by the Mobile Broadband service to indicate that registration mode information is available. |
| [IMbnRegistrationEvents::OnRegisterStateChange](..\mbnapi\nf-mbnapi-imbnregistrationevents-onregisterstatechange.md) | Notification method called by the Mobile Broadband service to indicate a change in the device's registration state. |
| [IMbnRegistrationEvents::OnSetRegisterModeComplete](..\mbnapi\nf-mbnapi-imbnregistrationevents-onsetregistermodecomplete.md) | Notification method called by the Mobile Broadband service to indicate that it has completed a set registration operation. |
| [IMbnServiceActivation::Activate](..\mbnapi\nf-mbnapi-imbnserviceactivation-activate.md) | Send the service activation request to the network. |
| [IMbnServiceActivationEvents::OnActivationComplete](..\mbnapi\nf-mbnapi-imbnserviceactivationevents-onactivationcomplete.md) | Notification method called by the Mobile Broadband service to indicate that a service activation request ahs completed. |
| [IMbnSignal::GetSignalError](..\mbnapi\nf-mbnapi-imbnsignal-getsignalerror.md) | Gets the received signal error rate. |
| [IMbnSignal::GetSignalStrength](..\mbnapi\nf-mbnapi-imbnsignal-getsignalstrength.md) | Gets the signal strength received by the device. |
| [IMbnSignalEvents::OnSignalStateChange](..\mbnapi\nf-mbnapi-imbnsignalevents-onsignalstatechange.md) | This notification method is called by the Mobile Broadband service to indicate that a signal quality update is available. |
| [IMbnSms::GetSmsConfiguration](..\mbnapi\nf-mbnapi-imbnsms-getsmsconfiguration.md) | Gets the SMS configuration of a device. |
| [IMbnSms::GetSmsStatus](..\mbnapi\nf-mbnapi-imbnsms-getsmsstatus.md) | Gets the SMS status for a device. |
| [IMbnSms::SetSmsConfiguration](..\mbnapi\nf-mbnapi-imbnsms-setsmsconfiguration.md) | Updates the SMS configuration for a device. |
| [IMbnSms::SmsDelete](..\mbnapi\nf-mbnapi-imbnsms-smsdelete.md) | Deletes a set of SMS messages from a device. |
| [IMbnSms::SmsRead](..\mbnapi\nf-mbnapi-imbnsms-smsread.md) | Reads a set of SMS messages from a device. |
| [IMbnSms::SmsSendCdmaPdu](..\mbnapi\nf-mbnapi-imbnsms-smssendcdmapdu.md) | Sends a message in CDMA binary format. |
| [IMbnSms::SmsSendCdma](..\mbnapi\nf-mbnapi-imbnsms-smssendcdma.md) | Sends a message in CDMA format. |
| [IMbnSms::SmsSendPdu](..\mbnapi\nf-mbnapi-imbnsms-smssendpdu.md) | Sends a message in PDU format. |
| [IMbnSmsConfiguration::get_CdmaShortMsgSize](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-get_cdmashortmsgsize.md) | Maximum CDMA short message character length. |
| [IMbnSmsConfiguration::get_MaxMessageIndex](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-get_maxmessageindex.md) | SMS message memory capacity. |
| [IMbnSmsConfiguration::get_ServiceCenterAddress](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-get_servicecenteraddress.md) | SMS default Service Center address. |
| [IMbnSmsConfiguration::get_SmsFormat](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-get_smsformat.md) | Format in which newly received SMS should be reported by the device. |
| [IMbnSmsConfiguration::put_ServiceCenterAddress](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-put_servicecenteraddress.md) | SMS default Service Center address. |
| [IMbnSmsConfiguration::put_SmsFormat](..\mbnapi\nf-mbnapi-imbnsmsconfiguration-put_smsformat.md) | Format in which newly received SMS should be reported by the device. |
| [IMbnSmsEvents::OnSetSmsConfigurationComplete](..\mbnapi\nf-mbnapi-imbnsmsevents-onsetsmsconfigurationcomplete.md) | Notification method signaling that a set SMS configuration operation has completed, or that the SMS subsystem is initialized and ready for operation. |
| [IMbnSmsEvents::OnSmsConfigurationChange](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmsconfigurationchange.md) | Notification method that indicates that SMS configuration has changed or is available. |
| [IMbnSmsEvents::OnSmsDeleteComplete](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmsdeletecomplete.md) | Notification method that signals the completion of an SMS deletion operation. |
| [IMbnSmsEvents::OnSmsNewClass0Message](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmsnewclass0message.md) | Notification method signaling the arrival of a new class 0/flash message. |
| [IMbnSmsEvents::OnSmsReadComplete](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmsreadcomplete.md) | Notification method indicating the completion of a message read operation. |
| [IMbnSmsEvents::OnSmsSendComplete](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmssendcomplete.md) | Notification method that indicates the completion of a message send operation. |
| [IMbnSmsEvents::OnSmsStatusChange](..\mbnapi\nf-mbnapi-imbnsmsevents-onsmsstatuschange.md) | Notification method indicating a change in the status of the message store. |
| [IMbnSmsReadMsgPdu::get_Index](..\mbnapi\nf-mbnapi-imbnsmsreadmsgpdu-get_index.md) | The index of the message in the device SMS store. |
| [IMbnSmsReadMsgPdu::get_PduData](..\mbnapi\nf-mbnapi-imbnsmsreadmsgpdu-get_pdudata.md) | The PDU message in hexadecimal format as used by GSM devices. |
| [IMbnSmsReadMsgPdu::get_Status](..\mbnapi\nf-mbnapi-imbnsmsreadmsgpdu-get_status.md) | The type of message. |
| [IMbnSmsReadMsgTextCdma::get_Address](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_address.md) | The mobile number associated with a message. |
| [IMbnSmsReadMsgTextCdma::get_EncodingID](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_encodingid.md) | The data encoding used in the message. |
| [IMbnSmsReadMsgTextCdma::get_Index](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_index.md) | The index of the message in device SMS memory. |
| [IMbnSmsReadMsgTextCdma::get_LanguageID](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_languageid.md) | The language used in the message. |
| [IMbnSmsReadMsgTextCdma::get_Message](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_message.md) | The contents of the message. |
| [IMbnSmsReadMsgTextCdma::get_SizeInCharacters](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_sizeincharacters.md) | The size in characters of the message. |
| [IMbnSmsReadMsgTextCdma::get_Status](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_status.md) | The type of message. |
| [IMbnSmsReadMsgTextCdma::get_Timestamp](..\mbnapi\nf-mbnapi-imbnsmsreadmsgtextcdma-get_timestamp.md) | The timestamp of a message. |
| [IMbnSubscriberInformation::get_SimIccID](..\mbnapi\nf-mbnapi-imbnsubscriberinformation-get_simiccid.md) | The SIM International circuit card number (SimICCID) for the device. |
| [IMbnSubscriberInformation::get_SubscriberID](..\mbnapi\nf-mbnapi-imbnsubscriberinformation-get_subscriberid.md) | The subscriber ID of the device. |
| [IMbnSubscriberInformation::get_TelephoneNumbers](..\mbnapi\nf-mbnapi-imbnsubscriberinformation-get_telephonenumbers.md) | The telephone numbers associated with the device. |
| [IMbnVendorSpecificEvents::OnEventNotification](..\mbnapi\nf-mbnapi-imbnvendorspecificevents-oneventnotification.md) | Notification method signaling a change event from the underlying Mobile Broadband device miniport driver. |
| [IMbnVendorSpecificEvents::OnSetVendorSpecificComplete](..\mbnapi\nf-mbnapi-imbnvendorspecificevents-onsetvendorspecificcomplete.md) | Notification method indicating that a vendor-specific operation has completed. |
| [IMbnVendorSpecificOperation::SetVendorSpecific](..\mbnapi\nf-mbnapi-imbnvendorspecificoperation-setvendorspecific.md) | Sends a request to the underlying Mobile Broadband device miniport driver. |
