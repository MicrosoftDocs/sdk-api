---
UID: NE:evcoll._EC_SUBSCRIPTION_CONFIGURATION_MODE
title: EC_SUBSCRIPTION_CONFIGURATION_MODE (evcoll.h)
description: Specifies different configuration modes that change the default settings for a subscription.
helpviewer_keywords: ["EC_SUBSCRIPTION_CONFIGURATION_MODE","EC_SUBSCRIPTION_CONFIGURATION_MODE enumeration","EcConfigurationModeCustom","EcConfigurationModeMinBandwidth","EcConfigurationModeMinLatency","EcConfigurationModeNormal","evcoll/EC_SUBSCRIPTION_CONFIGURATION_MODE","evcoll/EcConfigurationModeCustom","evcoll/EcConfigurationModeMinBandwidth","evcoll/EcConfigurationModeMinLatency","evcoll/EcConfigurationModeNormal","wec.ec_subscription_configuration_mode","wes.ec_subscription_configuration_mode"]
old-location: wec\ec_subscription_configuration_mode.htm
tech.root: WEC
ms.assetid: ec2c3006-c452-4dec-b3ed-a7a11f6456b3
ms.date: 12/05/2018
ms.keywords: EC_SUBSCRIPTION_CONFIGURATION_MODE, EC_SUBSCRIPTION_CONFIGURATION_MODE enumeration, EcConfigurationModeCustom, EcConfigurationModeMinBandwidth, EcConfigurationModeMinLatency, EcConfigurationModeNormal, evcoll/EC_SUBSCRIPTION_CONFIGURATION_MODE, evcoll/EcConfigurationModeCustom, evcoll/EcConfigurationModeMinBandwidth, evcoll/EcConfigurationModeMinLatency, evcoll/EcConfigurationModeNormal, wec.ec_subscription_configuration_mode, wes.ec_subscription_configuration_mode
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
req.typenames: EC_SUBSCRIPTION_CONFIGURATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EC_SUBSCRIPTION_CONFIGURATION_MODE
 - evcoll/_EC_SUBSCRIPTION_CONFIGURATION_MODE
 - EC_SUBSCRIPTION_CONFIGURATION_MODE
 - evcoll/EC_SUBSCRIPTION_CONFIGURATION_MODE
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
 - EC_SUBSCRIPTION_CONFIGURATION_MODE
---

# EC_SUBSCRIPTION_CONFIGURATION_MODE enumeration


## -description

The <b>EC_SUBSCRIPTION_CONFIGURATION_MODE</b> enumeration specifies different configuration modes that change the default settings for a subscription. Each configuration mode is used to define default settings for a different scenario, and sets the subscription delivery mode and default property values.

## -enum-fields

### -field EcConfigurationModeNormal:0

This mode is used when an administrator needs the events to be delivered reliably and for the subscription to work with minimal configuration, and when network usage is not a concern. This mode sets the default subscription delivery mode to pull subscriptions.

### -field EcConfigurationModeCustom

This subscription mode allows custom values for the DeliveryMode property, the DeliveryMaxItems property, the DeliveryMaxLatencyTime, and the HeartBeatInterval property.

### -field EcConfigurationModeMinLatency

This mode is used for alerts and critical events because it configures the subscription to send events as soon as they occur with minimal delay. This mode sets the default subscription delivery mode to push subscriptions.

### -field EcConfigurationModeMinBandwidth

This mode is used when network activity is controllable, and when network usage is expensive. This mode sets the default subscription delivery mode to push subscriptions.

## -remarks

The settings for each configuration mode can be found in the Event Collector registry located at: <pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>EventCollector</b>
                  <b>ConfigurationModes</b></pre>


For more information about the subscription delivery mode and properties see, <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_delivery_mode">EC_SUBSCRIPTION_DELIVERY_MODE</a> and  <a href="/windows/desktop/api/evcoll/ne-evcoll-ec_subscription_property_id">EC_SUBSCRIPTION_PROPERTY_ID</a>.
