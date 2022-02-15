---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005
title: WDSTRANSPORT_SERVICE_NOTIFICATION (wdstptmgmt.h)
description: Specifies what action needs to be taken when notifying WDS transport services, such as rereading their settings following a configuration change.
helpviewer_keywords: ["*PWDSTRANSPORT_SERVICE_NOTIFICATION","WDSTRANSPORT_SERVICE_NOTIFICATION","WDSTRANSPORT_SERVICE_NOTIFICATION enumeration [Windows Deployment Services]","WdsTptServiceNotifyReadSettings","WdsTptServiceNotifyUnknown","wds.wdstransport_service_notification","wdstptmgmt/WDSTRANSPORT_SERVICE_NOTIFICATION","wdstptmgmt/WdsTptServiceNotifyReadSettings","wdstptmgmt/WdsTptServiceNotifyUnknown"]
old-location: wds\wdstransport_service_notification.htm
tech.root: wds
ms.assetid: d239241d-efe9-409b-8425-c71382b27c05
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_SERVICE_NOTIFICATION, WDSTRANSPORT_SERVICE_NOTIFICATION, WDSTRANSPORT_SERVICE_NOTIFICATION enumeration [Windows Deployment Services], WdsTptServiceNotifyReadSettings, WdsTptServiceNotifyUnknown, wds.wdstransport_service_notification, wdstptmgmt/WDSTRANSPORT_SERVICE_NOTIFICATION, wdstptmgmt/WdsTptServiceNotifyReadSettings, wdstptmgmt/WdsTptServiceNotifyUnknown'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WDSTRANSPORT_SERVICE_NOTIFICATION, *PWDSTRANSPORT_SERVICE_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0005
 - PWDSTRANSPORT_SERVICE_NOTIFICATION
 - wdstptmgmt/PWDSTRANSPORT_SERVICE_NOTIFICATION
 - WDSTRANSPORT_SERVICE_NOTIFICATION
 - wdstptmgmt/WDSTRANSPORT_SERVICE_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_SERVICE_NOTIFICATION
---

# WDSTRANSPORT_SERVICE_NOTIFICATION enumeration


## -description

Specifies what action needs to be taken when notifying WDS transport services, such as rereading their settings following a configuration change.

## -enum-fields

### -field WdsTptServiceNotifyUnknown:0

Default value that indicates that the notification type is not known.

### -field WdsTptServiceNotifyReadSettings:1

Specifies that the WDS transport services should reread their settings to pick up recent updates.

