---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005
title: "__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005"
author: windows-sdk-content
description: Specifies what action needs to be taken when notifying WDS transport services, such as rereading their settings following a configuration change.
old-location: wds\wdstransport_service_notification.htm
old-project: Wds
ms.assetid: d239241d-efe9-409b-8425-c71382b27c05
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: "*PWDSTRANSPORT_SERVICE_NOTIFICATION, WDSTRANSPORT_SERVICE_NOTIFICATION, WDSTRANSPORT_SERVICE_NOTIFICATION enumeration [Windows Deployment Services], WdsTptServiceNotifyReadSettings, WdsTptServiceNotifyUnknown, __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005, wds.wdstransport_service_notification, wdstptmgmt/WDSTRANSPORT_SERVICE_NOTIFICATION, wdstptmgmt/WdsTptServiceNotifyReadSettings, wdstptmgmt/WdsTptServiceNotifyUnknown"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDSTRANSPORT_SERVICE_NOTIFICATION, *PWDSTRANSPORT_SERVICE_NOTIFICATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdstptmgmt.h
api_name:
-	WDSTRANSPORT_SERVICE_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005 enumeration


## -description


Specifies what action needs to be taken when notifying WDS transport services, such as rereading their settings following a configuration change. 


## -enum-fields




### -field WdsTptServiceNotifyUnknown

Default value that indicates that the notification type is not known.


### -field WdsTptServiceNotifyReadSettings

Specifies that the WDS transport services should reread their settings to pick up recent updates.

