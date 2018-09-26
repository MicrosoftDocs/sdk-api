---
UID: NE:credentialprovider._CREDENTIAL_PROVIDER_STATUS_ICON
title: "_CREDENTIAL_PROVIDER_STATUS_ICON"
author: windows-sdk-content
description: Indicates which status icon should be displayed.
old-location: shell\CREDENTIAL_PROVIDER_STATUS_ICON.htm
tech.root: shell
ms.assetid: 2aa5b5dc-4756-4eff-a7d8-97c8a1dce41b
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CPSI_ERROR, CPSI_NONE, CPSI_SUCCESS, CPSI_WARNING, CREDENTIAL_PROVIDER_STATUS_ICON, CREDENTIAL_PROVIDER_STATUS_ICON enumeration [Windows Shell], _CREDENTIAL_PROVIDER_STATUS_ICON, _shell_CREDENTIAL_PROVIDER_STATUS_ICON, credentialprovider/CPSI_ERROR, credentialprovider/CPSI_NONE, credentialprovider/CPSI_SUCCESS, credentialprovider/CPSI_WARNING, credentialprovider/CREDENTIAL_PROVIDER_STATUS_ICON, shell.CREDENTIAL_PROVIDER_STATUS_ICON
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credentialprovider.h
api_name:
 - CREDENTIAL_PROVIDER_STATUS_ICON
product: Windows
targetos: Windows
req.typenames: CREDENTIAL_PROVIDER_STATUS_ICON
req.redist: 
---

# _CREDENTIAL_PROVIDER_STATUS_ICON enumeration


## -description


Indicates which status icon should be displayed.


## -enum-fields




### -field CPSI_NONE

No icon indicated.


### -field CPSI_ERROR

Display the error icon.


### -field CPSI_WARNING

Display the warning icon.


### -field CPSI_SUCCESS

Reserved.


## -remarks



<b>CREDENTIAL_PROVIDER_STATUS_ICON</b> is not used starting in Windows 10.

As part of <a href="https://msdn.microsoft.com/en-us/library/Bb776030(v=VS.85).aspx">ReportResult</a>, a credential provider may specify a status icon to display. It is important to not that only Logon UI calls <b>ReportResult</b>, Credential UI does not.



