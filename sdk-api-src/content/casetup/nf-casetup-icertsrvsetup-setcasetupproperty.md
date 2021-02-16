---
UID: NF:casetup.ICertSrvSetup.SetCASetupProperty
title: ICertSrvSetup::SetCASetupProperty (casetup.h)
description: Sets a property value for a certification authority (CA) configuration.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","SetCASetupProperty method","ICertSrvSetup.SetCASetupProperty","ICertSrvSetup::SetCASetupProperty","SetCASetupProperty","SetCASetupProperty method [Security]","SetCASetupProperty method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::SetCASetupProperty","security.icertsrvsetup_setcasetupproperty"]
old-location: security\icertsrvsetup_setcasetupproperty.htm
tech.root: security
ms.assetid: 91df1926-a4b6-4ba2-ab59-0258293fc1c0
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetCASetupProperty method, ICertSrvSetup.SetCASetupProperty, ICertSrvSetup::SetCASetupProperty, SetCASetupProperty, SetCASetupProperty method [Security], SetCASetupProperty method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetCASetupProperty, security.icertsrvsetup_setcasetupproperty
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
 - ICertSrvSetup::SetCASetupProperty
 - casetup/ICertSrvSetup::SetCASetupProperty
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
 - ICertSrvSetup.SetCASetupProperty
---

# ICertSrvSetup::SetCASetupProperty


## -description

The <b>SetCASetupProperty</b> method sets a property value for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration.

## -parameters

### -param propertyId [in]

A <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a> constant that specifies the type of property to configure.

The following properties are set as a side effect of other methods and cannot be set directly with this method.

<b>ENUM_SETUPPROP_CANAME</b>
<b>ENUM_SETUPPROP_CADSSUFFIX</b>
<b>ENUM_SETUPPROP_EXPIRATIONDATE</b>
<b>ENUM_SETUPPROP_PARENTCANAME</b>
<b>ENUM_SETUPPROP_PARENTCAMACHINE</b>
<b>ENUM_SETUPPROP_DATABASEDIRECTORY</b>
<b>ENUM_SETUPPROP_LOGDIRECTORY</b>
<b>ENUM_SETUPPROP_SHAREDFOLDER</b>
<b>ENUM_SETUPPROP_WEBCAMACHINE</b>
<b>ENUM_SETUPPROP_WEBCANAME</b>

### -param pPropertyValue [in]

A pointer to a <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>