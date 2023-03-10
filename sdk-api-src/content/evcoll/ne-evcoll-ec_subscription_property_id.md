---
UID: NE:evcoll._EC_SUBSCRIPTION_PROPERTY_ID
title: EC_SUBSCRIPTION_PROPERTY_ID (evcoll.h)
description: Defines values to identify event subscription properties used for subscription configuration.
helpviewer_keywords: ["EC_SUBSCRIPTION_PROPERTY_ID","EC_SUBSCRIPTION_PROPERTY_ID enumeration","EcSubscriptionAllowedIssuerCAs","EcSubscriptionAllowedSourceDomainComputers","EcSubscriptionAllowedSubjects","EcSubscriptionCommonPassword","EcSubscriptionCommonUserName","EcSubscriptionConfigurationMode","EcSubscriptionContentFormat","EcSubscriptionCredentialsType","EcSubscriptionDeliveryMaxItems","EcSubscriptionDeliveryMaxLatencyTime","EcSubscriptionDeliveryMode","EcSubscriptionDeniedSubjects","EcSubscriptionDescription","EcSubscriptionDialect","EcSubscriptionEnabled","EcSubscriptionEventSourceAddress","EcSubscriptionEventSourceEnabled","EcSubscriptionEventSourcePassword","EcSubscriptionEventSourceUserName","EcSubscriptionEventSources","EcSubscriptionExpires","EcSubscriptionHeartbeatInterval","EcSubscriptionHostName","EcSubscriptionLocale","EcSubscriptionLogFile","EcSubscriptionPublisherName","EcSubscriptionQuery","EcSubscriptionReadExistingEvents","EcSubscriptionTransportName","EcSubscriptionTransportPort","EcSubscriptionType","EcSubscriptionURI","evcoll/EC_SUBSCRIPTION_PROPERTY_ID","evcoll/EcSubscriptionAllowedIssuerCAs","evcoll/EcSubscriptionAllowedSourceDomainComputers","evcoll/EcSubscriptionAllowedSubjects","evcoll/EcSubscriptionCommonPassword","evcoll/EcSubscriptionCommonUserName","evcoll/EcSubscriptionConfigurationMode","evcoll/EcSubscriptionContentFormat","evcoll/EcSubscriptionCredentialsType","evcoll/EcSubscriptionDeliveryMaxItems","evcoll/EcSubscriptionDeliveryMaxLatencyTime","evcoll/EcSubscriptionDeliveryMode","evcoll/EcSubscriptionDeniedSubjects","evcoll/EcSubscriptionDescription","evcoll/EcSubscriptionDialect","evcoll/EcSubscriptionEnabled","evcoll/EcSubscriptionEventSourceAddress","evcoll/EcSubscriptionEventSourceEnabled","evcoll/EcSubscriptionEventSourcePassword","evcoll/EcSubscriptionEventSourceUserName","evcoll/EcSubscriptionEventSources","evcoll/EcSubscriptionExpires","evcoll/EcSubscriptionHeartbeatInterval","evcoll/EcSubscriptionHostName","evcoll/EcSubscriptionLocale","evcoll/EcSubscriptionLogFile","evcoll/EcSubscriptionPublisherName","evcoll/EcSubscriptionQuery","evcoll/EcSubscriptionReadExistingEvents","evcoll/EcSubscriptionTransportName","evcoll/EcSubscriptionTransportPort","evcoll/EcSubscriptionType","evcoll/EcSubscriptionURI","wec.ec_subscription_property_id","wes.ec_subscription_property_id"]
old-location: wec\ec_subscription_property_id.htm
tech.root: WEC
ms.assetid: c70dca98-1c14-4c0c-9f2e-6241c463fe4e
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_PROPERTY_ID, EC_SUBSCRIPTION_PROPERTY_ID enumeration, EcSubscriptionAllowedIssuerCAs, EcSubscriptionAllowedSourceDomainComputers, EcSubscriptionAllowedSubjects, EcSubscriptionCommonPassword, EcSubscriptionCommonUserName, EcSubscriptionConfigurationMode, EcSubscriptionContentFormat, EcSubscriptionCredentialsType, EcSubscriptionDeliveryMaxItems, EcSubscriptionDeliveryMaxLatencyTime, EcSubscriptionDeliveryMode, EcSubscriptionDeniedSubjects, EcSubscriptionDescription, EcSubscriptionDialect, EcSubscriptionEnabled, EcSubscriptionEventSourceAddress, EcSubscriptionEventSourceEnabled, EcSubscriptionEventSourcePassword, EcSubscriptionEventSourceUserName, EcSubscriptionEventSources, EcSubscriptionExpires, EcSubscriptionHeartbeatInterval, EcSubscriptionHostName, EcSubscriptionLocale, EcSubscriptionLogFile, EcSubscriptionPublisherName, EcSubscriptionQuery, EcSubscriptionReadExistingEvents, EcSubscriptionTransportName, EcSubscriptionTransportPort, EcSubscriptionType, EcSubscriptionURI, evcoll/EC_SUBSCRIPTION_PROPERTY_ID, evcoll/EcSubscriptionAllowedIssuerCAs, evcoll/EcSubscriptionAllowedSourceDomainComputers, evcoll/EcSubscriptionAllowedSubjects, evcoll/EcSubscriptionCommonPassword, evcoll/EcSubscriptionCommonUserName, evcoll/EcSubscriptionConfigurationMode, evcoll/EcSubscriptionContentFormat, evcoll/EcSubscriptionCredentialsType, evcoll/EcSubscriptionDeliveryMaxItems, evcoll/EcSubscriptionDeliveryMaxLatencyTime, evcoll/EcSubscriptionDeliveryMode, evcoll/EcSubscriptionDeniedSubjects, evcoll/EcSubscriptionDescription, evcoll/EcSubscriptionDialect, evcoll/EcSubscriptionEnabled, evcoll/EcSubscriptionEventSourceAddress, evcoll/EcSubscriptionEventSourceEnabled, evcoll/EcSubscriptionEventSourcePassword, evcoll/EcSubscriptionEventSourceUserName, evcoll/EcSubscriptionEventSources, evcoll/EcSubscriptionExpires, evcoll/EcSubscriptionHeartbeatInterval, evcoll/EcSubscriptionHostName, evcoll/EcSubscriptionLocale, evcoll/EcSubscriptionLogFile, evcoll/EcSubscriptionPublisherName, evcoll/EcSubscriptionQuery, evcoll/EcSubscriptionReadExistingEvents, evcoll/EcSubscriptionTransportName, evcoll/EcSubscriptionTransportPort, evcoll/EcSubscriptionType, evcoll/EcSubscriptionURI, wec.ec_subscription_property_id, wes.ec_subscription_property_id
req.header: evcoll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: EC_SUBSCRIPTION_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_PROPERTY_ID
 - evcoll/_EC_SUBSCRIPTION_PROPERTY_ID
 - EC_SUBSCRIPTION_PROPERTY_ID
 - evcoll/EC_SUBSCRIPTION_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evcoll.h
api_name:
 - EC_SUBSCRIPTION_PROPERTY_ID
---

# EC_SUBSCRIPTION_PROPERTY_ID enumeration


## -description

The <b>EC_SUBSCRIPTION_PROPERTY_ID</b> enumeration defines values to identify event subscription properties used for subscription configuration.

## -enum-fields

### -field EcSubscriptionEnabled:0

The <b>Enabled</b> property of the subscription that is used to enable or disable the subscription or obtain the current status of a subscription. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeBoolean</a> value.

### -field EcSubscriptionEventSources

The <b>EventSources</b> property of the subscription that contains a collection of information about the local or remote computers (event sources) that can forward events to the  event collector. This property is a handle to an array (an  <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarObjectArrayPropertyHandle</a> value). This value is typically used for collector initiated subscriptions. It can be used for source initiated subscriptions to disable the collection of events from a particular event source.

### -field EcSubscriptionEventSourceAddress

The <b>EventSourceAddress</b> property of the subscription that contains the IP address or fully qualified domain name (FQDN) of the local or remote computer (event source) from which the events are collected. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionEventSourceEnabled

The <b>EventSourceEnabled</b> property of the subscription that is used to enable or disable an  event source.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeBoolean</a> value.

### -field EcSubscriptionEventSourceUserName

The <b>EventSourceUserName</b> property of the subscription that contains the user name, which is used by the remote computer (event source) to authenticate the user.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionEventSourcePassword

The <b>EventSourcePassword</b> property of the subscription that contains the password, which is used by the remote computer (event source) to authenticate the user.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionDescription

The <b>Description</b> property of the subscription that contains a description of the subscription.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionURI

The <b>URI</b> property of the subscription that contains the URI, which is used by WS-Management to connect to a computer. For example, the URI can be `http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel` for hardware events or
it can be `http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog` for events that are published in the event log.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionConfigurationMode

The <b>ConfigurationMode</b> property of the subscription that specifies how events are delivered to the subscription.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value from the <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_configuration_mode">EC_SUBSCRIPTION_CONFIGURATION_MODE</a> enumeration.

### -field EcSubscriptionExpires

The <b>Expires</b> property of the subscription  that contains the date when the subscription will  end. The maximum date that can be used is 3000-12-31T23:59:59.999Z. If this property is not defined, the subscription will not expire.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeDateTime</a> value.

### -field EcSubscriptionQuery

The <b>Query</b> property of the subscription that contains the query, which is  used by the event source for selecting events to forward to the event collector. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionTransportName

The <b>TransportName</b> property of the subscription  that specifies the type of transport, which is used to connect to the remote computer (event source).   This value can be either HTTP, which is the default, or it can be HTTPS. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionTransportPort

The <b>TransportPort</b> property of the subscription  that specifies the port number, which the transport uses to connect to the remote computer (event source).  The default port number for HTTP is 80 and the default port number for HTTPS is  443. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value.

### -field EcSubscriptionDeliveryMode

The <b>DeliveryMode</b> property of the subscription that specifies  whether events are delivered to the subscription with either a push or pull model.  This property is an <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_delivery_mode">EC_SUBSCRIPTION_DELIVERY_MODE</a> enumeration value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionDeliveryMaxItems

The <b>DeliveryMaxItems</b> property of the subscription that specifies the maximum number of events that can be batched when forwarded from the event sources.  When the <b>EcSubscriptionDeliveryMode</b> property is set to <b>EcDeliveryModePush</b>, this property determines the number of events that are included in a batch sent from the event source. When the <b>EcSubscriptionDeliveryMode</b> property is set to <b>EcDeliveryModePull</b>, this property determines the maximum number of items that will forwarded from an event source for each request. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value.

### -field EcSubscriptionDeliveryMaxLatencyTime

The <b>DeliveryMaxLatencyTime</b> property of the subscription that specifies how long, in milliseconds, the event source should wait before sending events (even if it did not collect enough events  to reach the maximum number of items). This value is used when the <b>EcSubscriptionDeliveryMode</b> property is set to  <b>EcDeliveryModePush</b>.   This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value.

### -field EcSubscriptionHeartbeatInterval

The <b>HeartbeatInterval</b> property of the subscription that defines the heartbeat time interval, in milliseconds, which is observed between the sent heartbeat messages.  When the <b>EcSubscriptionDeliveryMode</b> property is set to <b>EcDeliveryModePush</b>, the event collector uses this property to determine the availability of the event source. When the <b>EcSubscriptionDeliveryMode</b> property is set to <b>EcDeliveryModePull</b>, the event collector uses this property to determine the interval between queries to the event source. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeUInt32</a> value.

### -field EcSubscriptionLocale

The <b>Locale</b> property of the subscription that specifies the locale (for example, en-us) of the events.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionContentFormat

The <b>ContentFormat</b> property of the subscription that specifies the format in which the event content should be delivered.  This property is an <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_content_format">EC_SUBSCRIPTION_CONTENT_FORMAT</a> enumeration value.

### -field EcSubscriptionLogFile

The <b>LogFile</b> property of the subscription that specifies the log file where the events collected from the event sources will be stored.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionPublisherName

The <b>PublisherName</b> property of the subscription that contains the name of publisher that the event collector computer will raise events to the local log as. This is used when you want to collect events in a log other than the ForwardedEvents log. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionCredentialsType

The <b>CredentialsType</b> property of the subscription that specifies the type of credentials used in the event subscription.  This property is an <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_credentials_type">EC_SUBSCRIPTION_CREDENTIALS_TYPE</a> enumeration value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionCommonUserName

The <b>CommonUserName</b> property  of the subscription that contains the common user name, which is used by the local and remote computers to authenticate the user.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionCommonPassword

The <b>CommonPassword</b> property of the subscription that contains the common password, which is used by the local and remote computers to authenticate the user.  This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value. This property cannot be used for source initiated subscriptions.

### -field EcSubscriptionHostName

The <b>HostName</b> property of the subscription that specifies the fully qualified domain name (FQDN) of the local computer. This property is used by an event source to forward events and is used in scenarios that involve multihomed servers that may have multiple FQDNs. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value and must only be used for a push subscription.

### -field EcSubscriptionReadExistingEvents

The <b>ReadExistingEvents</b> property of the subscription that determines whether to collect existing events or not. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeBoolean</a> value.

### -field EcSubscriptionDialect

The <b>Dialect</b> property of the subscription that specifies the dialect of the query string. For example, the dialect for  SQL based filters  would be SQL, and the dialect for WMI based filters would be WQL. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionType

The <b>Type</b> property of the subscription that defines whether the subscription is initiated by  an event source or collector. This property is a <b>EC_SUBSCRPTION_TYPE</b> value.

### -field EcSubscriptionAllowedIssuerCAs

The <b>AllowedIssuerCAs</b> property of the subscription that contains the certificate authorities (CAs) allowed if the subscription uses certificate-based authentication. This is used for source initiated subscriptions. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionAllowedSubjects

The <b>AllowedSubjects</b> property of the subscription that contains the subjects that are allowed for the subscription.  This is used for source initiated subscriptions.  The subject specifies names, such as domain names, for all the event source computers that are allowed in the subscription. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionDeniedSubjects

The <b>DeniedSubjects</b> property of the subscription that contains the subjects that are not allowed for the subscription.  This is used for source initiated subscriptions.  The subject specifies names, such as domain names, for all the event source computers that are not allowed in the subscription. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionAllowedSourceDomainComputers

The <b>AllowedSourceDomainComputers</b> property of the subscription that contains the source computers that are allowed to send events to the collector computer defined by an SDDL string. This property is an <a href="/windows/desktop/api/evcoll/ns-evcoll-ec_variant">EcVarTypeString</a> value.

### -field EcSubscriptionPropertyIdEND
