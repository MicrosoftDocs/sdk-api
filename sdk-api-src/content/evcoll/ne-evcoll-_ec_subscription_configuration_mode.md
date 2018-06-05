---
UID: NE:evcoll._EC_SUBSCRIPTION_CONFIGURATION_MODE
title: "_EC_SUBSCRIPTION_CONFIGURATION_MODE"
author: windows-sdk-content
description: Specifies different configuration modes that change the default settings for a subscription.
old-location: wec\ec_subscription_configuration_mode.htm
old-project: WEC
ms.assetid: ec2c3006-c452-4dec-b3ed-a7a11f6456b3
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: EC_SUBSCRIPTION_CONFIGURATION_MODE, EC_SUBSCRIPTION_CONFIGURATION_MODE enumeration, EcConfigurationModeCustom, EcConfigurationModeMinBandwidth, EcConfigurationModeMinLatency, EcConfigurationModeNormal, _EC_SUBSCRIPTION_CONFIGURATION_MODE, evcoll/EC_SUBSCRIPTION_CONFIGURATION_MODE, evcoll/EcConfigurationModeCustom, evcoll/EcConfigurationModeMinBandwidth, evcoll/EcConfigurationModeMinLatency, evcoll/EcConfigurationModeNormal, wec.ec_subscription_configuration_mode, wes.ec_subscription_configuration_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: EC_SUBSCRIPTION_CONFIGURATION_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evcoll.h
api_name:
-	EC_SUBSCRIPTION_CONFIGURATION_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EC_SUBSCRIPTION_CONFIGURATION_MODE enumeration


## -description


The <b>EC_SUBSCRIPTION_CONFIGURATION_MODE</b> enumeration specifies different configuration modes that change the default settings for a subscription. Each configuration mode is used to define default settings for a different scenario, and sets the subscription delivery mode and default property values.


## -enum-fields




### -field EcConfigurationModeNormal

This mode is used when an administrator needs the events to be delivered reliably and for the subscription to work with minimal configuration, and when network usage is not a concern. This mode sets the default subscription delivery mode to pull subscriptions.


### -field EcConfigurationModeCustom

This subscription mode allows custom values for the DeliveryMode property, the DeliveryMaxItems property, the DeliveryMaxLatencyTime, and the HeartBeatInterval property.


### -field EcConfigurationModeMinLatency

This mode is used for alerts and critical events because it configures the subscription to send events as soon as they occur with minimal delay. This mode sets the default subscription delivery mode to push subscriptions.


### -field EcConfigurationModeMinBandwidth

This mode is used when network activity is controllable, and when network usage is expensive. This mode sets the default subscription delivery mode to push subscriptions.


## -remarks



The settings for each configuration mode can be found in the Event Collector registry located at: <pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>EventCollector</b>
                  <b>ConfigurationModes</b></pre>


For more information about the subscription delivery mode and properties see, <a href="https://msdn.microsoft.com/ece884d6-df3c-44d0-a10c-affcf3107148">EC_SUBSCRIPTION_DELIVERY_MODE</a> and  <a href="https://msdn.microsoft.com/c70dca98-1c14-4c0c-9f2e-6241c463fe4e">EC_SUBSCRIPTION_PROPERTY_ID</a>.



