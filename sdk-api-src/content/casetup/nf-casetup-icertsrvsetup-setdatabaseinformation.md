---
UID: NF:casetup.ICertSrvSetup.SetDatabaseInformation
title: ICertSrvSetup::SetDatabaseInformation (casetup.h)
author: windows-sdk-content
description: Sets the database related information for the certification authority (CA) role.
old-location: security\icertsrvsetup_setdatabaseinformation.htm
tech.root: SecCrypto
ms.assetid: ae690d59-21fe-4429-8e80-ee2ce19a7090
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetDatabaseInformation method, ICertSrvSetup.SetDatabaseInformation, ICertSrvSetup::SetDatabaseInformation, SetDatabaseInformation, SetDatabaseInformation method [Security], SetDatabaseInformation method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetDatabaseInformation, security.icertsrvsetup_setdatabaseinformation
ms.topic: method
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.SetDatabaseInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::SetDatabaseInformation


## -description


The <b>SetDatabaseInformation</b> method sets the database related information for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) role.


## -parameters




### -param bstrDBDirectory [in]

A string that contains the name of the directory where the CA database files will be stored. This parameter must not be <b>NULL</b> or an empty string.


### -param bstrLogDirectory [in]

A string that contains the name of the directory where the CA database log files will be stored. This parameter must not be <b>NULL</b> or an empty string.


### -param bstrSharedFolder [in]

This parameter is reserved for future use and must be <b>NULL</b> or an empty string.


### -param bForceOverwrite [in]

A value that indicates whether to overwrite any existing database files in the specified directory. A value of <b>VARIANT_TRUE</b> specifies to overwrite existing files.


## -remarks



The <b>SetDatabaseInformation</b> method creates the specified directories if they do not exist.

Upon failure, the <b>SetDatabaseInformation</b> method might set additional error information in the <a href="https://msdn.microsoft.com/462fb4a6-2aad-46d4-98e0-32c095eff5c7">CAErrorId</a> and <a href="https://msdn.microsoft.com/154397f8-aa0e-4d74-b18e-b68b46fdfcdb">CAErrorString</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

