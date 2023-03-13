---
UID: NF:certadm.IOCSPCAConfiguration.put_ReminderDuration
title: IOCSPCAConfiguration::put_ReminderDuration (certadm.h)
description: Gets or sets the percentage of a signing certificate lifetime after which a warning event is logged. (Put)
helpviewer_keywords: ["IOCSPCAConfiguration interface [Security]","ReminderDuration property","IOCSPCAConfiguration.ReminderDuration","IOCSPCAConfiguration.put_ReminderDuration","IOCSPCAConfiguration::ReminderDuration","IOCSPCAConfiguration::get_ReminderDuration","IOCSPCAConfiguration::put_ReminderDuration","ReminderDuration property [Security]","ReminderDuration property [Security]","IOCSPCAConfiguration interface","certadm/IOCSPCAConfiguration::ReminderDuration","certadm/IOCSPCAConfiguration::get_ReminderDuration","certadm/IOCSPCAConfiguration::put_ReminderDuration","put_ReminderDuration","security.iocspcaconfiguration_reminderduration_method"]
old-location: security\iocspcaconfiguration_reminderduration_method.htm
tech.root: security
ms.assetid: 861289e7-b2f1-433f-a896-47f4b161712e
ms.date: 12/05/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ReminderDuration property, IOCSPCAConfiguration.ReminderDuration, IOCSPCAConfiguration.put_ReminderDuration, IOCSPCAConfiguration::ReminderDuration, IOCSPCAConfiguration::get_ReminderDuration, IOCSPCAConfiguration::put_ReminderDuration, ReminderDuration property [Security], ReminderDuration property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ReminderDuration, certadm/IOCSPCAConfiguration::get_ReminderDuration, certadm/IOCSPCAConfiguration::put_ReminderDuration, put_ReminderDuration, security.iocspcaconfiguration_reminderduration_method
req.header: certadm.h
req.include-header: Certserv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPCAConfiguration::put_ReminderDuration
 - certadm/IOCSPCAConfiguration::put_ReminderDuration
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPCAConfiguration.ReminderDuration
 - IOCSPCAConfiguration.get_ReminderDuration
 - IOCSPCAConfiguration.put_ReminderDuration
---

# IOCSPCAConfiguration::put_ReminderDuration


## -description

The <b>ReminderDuration</b> property gets or sets the percentage of a signing certificate lifetime after which a warning event is logged.

This property is read/write.

## -parameters

## -remarks

Percentage values must be in the range 0 through 100; the default value is 90. An Online Certificate Status Protocol (OCSP) responder service includes a service-wide value having this default.

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspcaconfiguration">IOCSPCAConfiguration</a>
