---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0001
title: WDSTRANSPORT_FEATURE_FLAGS (wdstptmgmt.h)
description: Indicates which WDS features are installed on the WDS server.
helpviewer_keywords: ["*PWDSTRANSPORT_FEATURE_FLAGS","WDSTRANSPORT_FEATURE_FLAGS","WDSTRANSPORT_FEATURE_FLAGS enumeration [Windows Deployment Services]","WdsTptFeatureAdminPack","WdsTptFeatureDeploymentServer","WdsTptFeatureTransportServer","wds.wdstransport_feature_flags","wdstptmgmt/WDSTRANSPORT_FEATURE_FLAGS","wdstptmgmt/WdsTptFeatureAdminPack","wdstptmgmt/WdsTptFeatureDeploymentServer","wdstptmgmt/WdsTptFeatureTransportServer"]
old-location: wds\wdstransport_feature_flags.htm
tech.root: wds
ms.assetid: 60ce036d-7875-4fa7-8d7e-20a9faf63291
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_FEATURE_FLAGS, WDSTRANSPORT_FEATURE_FLAGS, WDSTRANSPORT_FEATURE_FLAGS enumeration [Windows Deployment Services], WdsTptFeatureAdminPack, WdsTptFeatureDeploymentServer, WdsTptFeatureTransportServer, wds.wdstransport_feature_flags, wdstptmgmt/WDSTRANSPORT_FEATURE_FLAGS, wdstptmgmt/WdsTptFeatureAdminPack, wdstptmgmt/WdsTptFeatureDeploymentServer, wdstptmgmt/WdsTptFeatureTransportServer'
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
req.typenames: WDSTRANSPORT_FEATURE_FLAGS, *PWDSTRANSPORT_FEATURE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0001
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0001
 - PWDSTRANSPORT_FEATURE_FLAGS
 - wdstptmgmt/PWDSTRANSPORT_FEATURE_FLAGS
 - WDSTRANSPORT_FEATURE_FLAGS
 - wdstptmgmt/WDSTRANSPORT_FEATURE_FLAGS
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
 - WDSTRANSPORT_FEATURE_FLAGS
---

# WDSTRANSPORT_FEATURE_FLAGS enumeration


## -description

Indicates which WDS features are installed on the WDS server.

## -enum-fields

### -field WdsTptFeatureAdminPack:0x1

The server has the WDS administrator pack installed. This feature is used for managing WDS local or remote WDS servers.

### -field WdsTptFeatureTransportServer:0x2

The server has the WDS Transport Server role installed. This feature provides a generic, extensible transport platform that can be used by any application. Generally, this role has to be installed on the server for most of the WdsTptMgmt functionality to be available. Without this role, only limited functionality about the server's install state would be available through WdsTptMgmt.

### -field WdsTptFeatureDeploymentServer:0x4

The server has the WDS Deployment Server role installed. This feature allows administrators to add operating system images to the server and configure it to allow PXE-booting clients to enumerate and install these images.

