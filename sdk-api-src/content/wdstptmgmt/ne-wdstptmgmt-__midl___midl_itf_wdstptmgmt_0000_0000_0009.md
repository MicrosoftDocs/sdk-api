---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009
title: "__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009"
author: windows-sdk-content
description: Configures which WDS components have diagnostics enabled. WDS diagnostics log events to the system event log.
old-location: wds\wdstransport_diagnostics_component_flags.htm
old-project: Wds
ms.assetid: 9c6aa422-b5b3-4fe8-a1ca-f401a3c5a1fb
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: "*PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS enumeration [Windows Deployment Services], WdsTptDiagnosticsComponentImageServer, WdsTptDiagnosticsComponentMulticast, WdsTptDiagnosticsComponentPxe, WdsTptDiagnosticsComponentTftp, __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009, wds.wdstransport_diagnostics_component_flags, wdstptmgmt/WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, wdstptmgmt/WdsTptDiagnosticsComponentImageServer, wdstptmgmt/WdsTptDiagnosticsComponentMulticast, wdstptmgmt/WdsTptDiagnosticsComponentPxe, wdstptmgmt/WdsTptDiagnosticsComponentTftp"
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
tech.root: 
req.typenames: WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS, *PWDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdstptmgmt.h
api_name:
 - WDSTRANSPORT_DIAGNOSTICS_COMPONENT_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0009 enumeration


## -description


Configures which WDS components have diagnostics enabled. WDS diagnostics log events to the system event log.


## -enum-fields




### -field WdsTptDiagnosticsComponentPxe

Diagnostics are enabled for the PXE component of WDS, which answers requests from clients performing a PXE network boot. This component is typically used by the WDS Deployment Server role but is also available for various third-party applications that use the WDS Transport Server role.


### -field WdsTptDiagnosticsComponentTftp

Diagnostics are enabled for the TFTP component of WDS, which handles simple file transfers from clients that are typically in a pre-boot environment. This component is typically used by the WDS Deployment Server role but is also available for various third-party applications that use the WDS Transport Server role.


### -field WdsTptDiagnosticsComponentImageServer

Diagnostics are enabled for the Image Server component of WDS, which handles client requests for enumerating operating system images on the server. This component is typically used by the WDS Deployment Server role.


### -field WdsTptDiagnosticsComponentMulticast

Diagnostics are enabled for the Multicast component of WDS, which handles multicast file transfers from clients.

