---
UID: NF:certadm.IOCSPCAConfiguration.get_ReminderDuration
title: IOCSPCAConfiguration::get_ReminderDuration
author: windows-sdk-content
description: Gets or sets the percentage of a signing certificate lifetime after which a warning event is logged.
old-location: security\iocspcaconfiguration_reminderduration_method.htm
old-project: seccrypto
ms.assetid: 861289e7-b2f1-433f-a896-47f4b161712e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOCSPCAConfiguration interface [Security],ReminderDuration property, IOCSPCAConfiguration.ReminderDuration, IOCSPCAConfiguration.get_ReminderDuration, IOCSPCAConfiguration::ReminderDuration, IOCSPCAConfiguration::get_ReminderDuration, IOCSPCAConfiguration::put_ReminderDuration, ReminderDuration property [Security], ReminderDuration property [Security],IOCSPCAConfiguration interface, certadm/IOCSPCAConfiguration::ReminderDuration, certadm/IOCSPCAConfiguration::get_ReminderDuration, certadm/IOCSPCAConfiguration::put_ReminderDuration, get_ReminderDuration, security.iocspcaconfiguration_reminderduration_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certadm.h
req.include-header: Certserv.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
---

# IOCSPCAConfiguration::get_ReminderDuration


## -description


The <b>ReminderDuration</b> property gets or sets the percentage of a signing certificate lifetime after which a warning event is logged.

This property is read/write.


## -parameters


## -remarks



Percentage values must be in the range 0 through 100; the default value is 90. An Online Certificate Status Protocol (OCSP) responder service includes a service-wide value having this default.




## -see-also




<a href="https://msdn.microsoft.com/57900e1e-9c51-4c1b-aa42-634b6c3a9999">IOCSPCAConfiguration</a>
 

 

