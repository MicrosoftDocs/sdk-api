---
UID: NF:casetup.ICertSrvSetup.SetDatabaseInformation
title: ICertSrvSetup::SetDatabaseInformation (casetup.h)
description: Sets the database related information for the certification authority (CA) role.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","SetDatabaseInformation method","ICertSrvSetup.SetDatabaseInformation","ICertSrvSetup::SetDatabaseInformation","SetDatabaseInformation","SetDatabaseInformation method [Security]","SetDatabaseInformation method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::SetDatabaseInformation","security.icertsrvsetup_setdatabaseinformation"]
old-location: security\icertsrvsetup_setdatabaseinformation.htm
tech.root: security
ms.assetid: ae690d59-21fe-4429-8e80-ee2ce19a7090
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetDatabaseInformation method, ICertSrvSetup.SetDatabaseInformation, ICertSrvSetup::SetDatabaseInformation, SetDatabaseInformation, SetDatabaseInformation method [Security], SetDatabaseInformation method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetDatabaseInformation, security.icertsrvsetup_setdatabaseinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::SetDatabaseInformation
 - casetup/ICertSrvSetup::SetDatabaseInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.SetDatabaseInformation
---

# ICertSrvSetup::SetDatabaseInformation


## -description

The <b>SetDatabaseInformation</b> method sets the database related information for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) role.

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

Upon failure, the <b>SetDatabaseInformation</b> method might set additional error information in the <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorid">CAErrorId</a> and <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorstring">CAErrorString</a> properties.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>