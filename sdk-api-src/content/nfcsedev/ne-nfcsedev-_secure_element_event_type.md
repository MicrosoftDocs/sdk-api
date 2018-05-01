---
UID: NE:nfcsedev._SECURE_ELEMENT_EVENT_TYPE
title: "_SECURE_ELEMENT_EVENT_TYPE"
author: windows-driver-content
description: Indicates the type of secure element events.
old-location: nfpdrivers\_secure_element_event_type.htm
old-project: nfpdrivers
ms.assetid: 45DCE635-6F28-4BE1-8362-568409FA8B1B
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSECURE_ELEMENT_EVENT_TYPE, ApplicationSelected, ExternalReaderArrival, ExternalReaderDeparture, HceActivated, HceDeactivated, SECURE_ELEMENT_EVENT_TYPE, Transaction, _SECURE_ELEMENT_EVENT_TYPE, _SECURE_ELEMENT_EVENT_TYPE enumeration [Near-Field Proximity Drivers], nfcsedev/ApplicationSelected, nfcsedev/ExternalReaderArrival, nfcsedev/ExternalReaderDeparture, nfcsedev/HceActivated, nfcsedev/HceDeactivated, nfcsedev/Transaction, nfcsedev/_SECURE_ELEMENT_EVENT_TYPE, nfpdrivers._secure_element_event_type"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: nfcsedev.h
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
req.typenames: SECURE_ELEMENT_EVENT_TYPE, *PSECURE_ELEMENT_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcsedev.h
api_name:
-	SECURE_ELEMENT_EVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SECURE_ELEMENT_EVENT_TYPE enumeration


## -description


Indicates the type of secure element events.


## -enum-fields




### -field ExternalReaderArrival

This event is fired when an external reader has established a connection with the indicated secure element. No other parameters are given for this event.


### -field ExternalReaderDeparture

This event is fired when an external reader has terminated a connection with the indicated secure element. No other parameters are given for this event.


### -field ApplicationSelected

This event is fired when the external reader has issued a “SELECT” command to select an application on the specified secure element. Additionally, the event notification includes the application ID (AID) of the selected application. Not all types of secure elements support the ability to raise this event.


### -field Transaction

This event is fired when an application that is operating within the secure element notifies the controller that some form of action has occurred. This event sends a list of parameters that is coded in BER-TLV fields. This event is mapped to EVT_TRANSACTION.


### -field HceActivated

This event is fired when a listen mode interface is activated to the device host. This event sends the current connection ID, activated RF protocol, and technology.


### -field HceDeactivated

This event is fired when a current active HCE session is terminated. This event sends the currently terminated connection ID.

