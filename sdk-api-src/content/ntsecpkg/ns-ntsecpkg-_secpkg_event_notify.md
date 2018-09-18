---
UID: NS:ntsecpkg._SECPKG_EVENT_NOTIFY
title: "_SECPKG_EVENT_NOTIFY"
author: windows-sdk-content
description: The SECPKG_EVENT_NOTIFY structure contains information about security events. This structure is passed to a function registered to receive event notifications. Event notification functions are registered by calling the RegisterNotification function.
old-location: security\secpkg_event_notify.htm
tech.root: secauthn
ms.assetid: 68516a5a-940f-48be-ba9c-5e72d23bc737
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PSECPKG_EVENT_NOTIFY, PSECPKG_EVENT_NOTIFY, PSECPKG_EVENT_NOTIFY structure pointer [Security], SECPKG_EVENT_NOTIFY, SECPKG_EVENT_NOTIFY structure [Security], _SECPKG_EVENT_NOTIFY, _ssp_secpkg_event_notify, ntsecpkg/PSECPKG_EVENT_NOTIFY, ntsecpkg/SECPKG_EVENT_NOTIFY, security.secpkg_event_notify"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_EVENT_NOTIFY
product: Windows
targetos: Windows
req.typenames: SECPKG_EVENT_NOTIFY, *PSECPKG_EVENT_NOTIFY
req.redist: 
---

# _SECPKG_EVENT_NOTIFY structure


## -description


The <b>SECPKG_EVENT_NOTIFY</b> structure contains information about security events. This structure is passed to a function registered to receive event notifications. Event notification functions are registered by calling the 
<a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> function.


## -struct-fields




### -field EventClass

The event class.


### -field Reserved

Reserved.


### -field EventDataSize

The size of the <b>EventData</b> member.


### -field EventData

The event details.


### -field PackageParameter

Information specified as the <i>Parameter</i> value when <a href="https://msdn.microsoft.com/689a1956-5eab-4eec-93ef-5ddcef6546ee">RegisterNotification</a> is called to register for notification.

