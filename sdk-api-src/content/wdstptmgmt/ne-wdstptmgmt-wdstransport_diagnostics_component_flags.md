---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009
title: WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS (wdstptmgmt.h)
description: Configures which WDS components have diagnostics enabled. WDS diagnostics log events to the system event log.
helpviewer_keywords: ["*PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS","WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS","WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS enumeration [Windows Deployment Services]","WdsTptDiagnosticsComponentImageServer","WdsTptDiagnosticsComponentMulticast","WdsTptDiagnosticsComponentPxe","WdsTptDiagnosticsComponentTftp","wds.wdstransport_diagnostics_component_flags","wdstptmgmt/WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS","wdstptmgmt/WdsTptDiagnosticsComponentImageServer","wdstptmgmt/WdsTptDiagnosticsComponentMulticast","wdstptmgmt/WdsTptDiagnosticsComponentPxe","wdstptmgmt/WdsTptDiagnosticsComponentTftp"]
old-location: wds\wdstransport_diagnostics_component_flags.htm
tech.root: wds
ms.assetid: 9c6aa422-b5b3-4fe8-a1ca-f401a3c5a1fb
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS enumeration [Windows Deployment Services], WdsTptDiagnosticsComponentImageServer, WdsTptDiagnosticsComponentMulticast, WdsTptDiagnosticsComponentPxe, WdsTptDiagnosticsComponentTftp, wds.wdstransport_diagnostics_component_flags, wdstptmgmt/WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, wdstptmgmt/WdsTptDiagnosticsComponentImageServer, wdstptmgmt/WdsTptDiagnosticsComponentMulticast, wdstptmgmt/WdsTptDiagnosticsComponentPxe, wdstptmgmt/WdsTptDiagnosticsComponentTftp'
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
req.typenames: WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, *PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009
 - PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
 - wdstptmgmt/PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
 - WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
 - wdstptmgmt/WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
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
 - WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
---

# WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS enumeration


## -description

Configures which WDS components have diagnostics enabled. WDS diagnostics log events to the system event log.

## -enum-fields

### -field WdsTptDiagnosticsComponentPxe:0x1

Diagnostics are enabled for the PXE component of WDS, which answers requests from clients performing a PXE network boot. This component is typically used by the WDS Deployment Server role but is also available for various third-party applications that use the WDS Transport Server role.

### -field WdsTptDiagnosticsComponentTftp:0x2

Diagnostics are enabled for the TFTP component of WDS, which handles simple file transfers from clients that are typically in a pre-boot environment. This component is typically used by the WDS Deployment Server role but is also available for various third-party applications that use the WDS Transport Server role.

### -field WdsTptDiagnosticsComponentImageServer:0x4

Diagnostics are enabled for the Image Server component of WDS, which handles client requests for enumerating operating system images on the server. This component is typically used by the WDS Deployment Server role.

### -field WdsTptDiagnosticsComponentMulticast:0x8

Diagnostics are enabled for the Multicast component of WDS, which handles multicast file transfers from clients.

