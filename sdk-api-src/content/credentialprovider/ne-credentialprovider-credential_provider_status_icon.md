---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_STATUS_ICON
title: CREDENTIAL_PROVIDER_STATUS_ICON (credentialprovider.h)
description: Indicates which status icon should be displayed.
helpviewer_keywords: ["CPSI_ERROR","CPSI_NONE","CPSI_SUCCESS","CPSI_WARNING","CREDENTIAL_PROVIDER_STATUS_ICON","CREDENTIAL_PROVIDER_STATUS_ICON enumeration [Windows Shell]","_shell_CREDENTIAL_PROVIDER_STATUS_ICON","credentialprovider/CPSI_ERROR","credentialprovider/CPSI_NONE","credentialprovider/CPSI_SUCCESS","credentialprovider/CPSI_WARNING","credentialprovider/CREDENTIAL_PROVIDER_STATUS_ICON","shell.CREDENTIAL_PROVIDER_STATUS_ICON"]
old-location: shell\CREDENTIAL_PROVIDER_STATUS_ICON.htm
tech.root: shell
ms.assetid: 2aa5b5dc-4756-4eff-a7d8-97c8a1dce41b
ms.date: 12/05/2018
ms.keywords: CPSI_ERROR, CPSI_NONE, CPSI_SUCCESS, CPSI_WARNING, CREDENTIAL_PROVIDER_STATUS_ICON, CREDENTIAL_PROVIDER_STATUS_ICON enumeration [Windows Shell], _shell_CREDENTIAL_PROVIDER_STATUS_ICON, credentialprovider/CPSI_ERROR, credentialprovider/CPSI_NONE, credentialprovider/CPSI_SUCCESS, credentialprovider/CPSI_WARNING, credentialprovider/CREDENTIAL_PROVIDER_STATUS_ICON, shell.CREDENTIAL_PROVIDER_STATUS_ICON
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_STATUS_ICON
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREDENTIAL_PROVIDER_STATUS_ICON
 - credentialprovider/_CREDENTIAL_PROVIDER_STATUS_ICON
 - CREDENTIAL_PROVIDER_STATUS_ICON
 - credentialprovider/CREDENTIAL_PROVIDER_STATUS_ICON
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_STATUS_ICON
---

# CREDENTIAL_PROVIDER_STATUS_ICON enumeration


## -description

Indicates which status icon should be displayed.

## -enum-fields

### -field CPSI_NONE:0

No icon indicated.

### -field CPSI_ERROR

Display the error icon.

### -field CPSI_WARNING

Display the warning icon.

### -field CPSI_SUCCESS

Reserved.

## -remarks

<b>CREDENTIAL_PROVIDER_STATUS_ICON</b> is not used starting in Windows 10.

As part of <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovidercredential-reportresult">ReportResult</a>, a credential provider may specify a status icon to display. It is important to not that only Logon UI calls <b>ReportResult</b>, Credential UI does not.
