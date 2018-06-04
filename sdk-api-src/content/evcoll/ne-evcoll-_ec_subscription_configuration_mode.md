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



