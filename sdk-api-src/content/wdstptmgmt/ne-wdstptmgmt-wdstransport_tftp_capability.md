---
UID: NE:wdstptmgmt.__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0012
title: WDSTRANSPORT_TFTP_CAPABILITY (wdstptmgmt.h)
description: Indicates which features are supported by the WDS TFTP server.
helpviewer_keywords: ["*PWDSTRANSPORT_TFTP_CAPABILITY","WDSTRANSPORT_TFTP_CAPABILITY","WDSTRANSPORT_TFTP_CAPABILITY enumeration [Windows Deployment Services]","WDSTRANSPORT_TFTP_CAPABILITY","*PWDSTRANSPORT_TFTP_CAPABILITY","WDSTRANSPORT_TFTP_CAPABILITY","*PWDSTRANSPORT_TFTP_CAPABILITY enumeration [Windows Deployment Services]","WdsTptTftpCapMaximumBlockSize","WdsTptTftpCapVariableWindow","wds.wdstransport_tftp_capability","wdstptmgmt/WDSTRANSPORT_TFTP_CAPABILITY","wdstptmgmt/WdsTptTftpCapMaximumBlockSize","wdstptmgmt/WdsTptTftpCapVariableWindow"]
old-location: wds\wdstransport_tftp_capability.htm
tech.root: wds
ms.assetid: 3D8F193B-6EEA-4E40-A53C-EB0768E0DE83
ms.date: 12/05/2018
ms.keywords: '*PWDSTRANSPORT_TFTP_CAPABILITY, WDSTRANSPORT_TFTP_CAPABILITY, WDSTRANSPORT_TFTP_CAPABILITY enumeration [Windows Deployment Services], WDSTRANSPORT_TFTP_CAPABILITY,*PWDSTRANSPORT_TFTP_CAPABILITY, WDSTRANSPORT_TFTP_CAPABILITY,*PWDSTRANSPORT_TFTP_CAPABILITY enumeration [Windows Deployment Services], WdsTptTftpCapMaximumBlockSize, WdsTptTftpCapVariableWindow, wds.wdstransport_tftp_capability, wdstptmgmt/WDSTRANSPORT_TFTP_CAPABILITY, wdstptmgmt/WdsTptTftpCapMaximumBlockSize, wdstptmgmt/WdsTptTftpCapVariableWindow'
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wdstptmgmt_0000_0000_0012
 - wdstptmgmt/__MIDL___MIDL_itf_wdstptmgmt_0000_0000_0012
 - PWDSTRANSPORT_TFTP_CAPABILITY
 - wdstptmgmt/PWDSTRANSPORT_TFTP_CAPABILITY
 - WDSTRANSPORT_TFTP_CAPABILITY
 - wdstptmgmt/WDSTRANSPORT_TFTP_CAPABILITY
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
 - WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
---

# WDSTRANSPORT_TFTP_CAPABILITY enumeration


## -description

Indicates which features are supported by the WDS TFTP server.

## -enum-fields

### -field WdsTptTftpCapMaximumBlockSize:0x1

Indicates that the maximum block size used by the server can be configured.

### -field WdsTptTftpCapVariableWindow:0x2

Indicates that the server supports variable-window TFTP extension.

