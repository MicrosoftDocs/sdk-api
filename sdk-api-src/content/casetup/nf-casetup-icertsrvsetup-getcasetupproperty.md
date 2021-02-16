---
UID: NF:casetup.ICertSrvSetup.GetCASetupProperty
title: ICertSrvSetup::GetCASetupProperty (casetup.h)
description: Gets a property value for a certification authority (CA) configuration.
helpviewer_keywords: ["GetCASetupProperty","GetCASetupProperty method [Security]","GetCASetupProperty method [Security]","ICertSrvSetup interface","ICertSrvSetup interface [Security]","GetCASetupProperty method","ICertSrvSetup.GetCASetupProperty","ICertSrvSetup::GetCASetupProperty","casetup/ICertSrvSetup::GetCASetupProperty","security.icertsrvsetup_getcasetupproperty"]
old-location: security\icertsrvsetup_getcasetupproperty.htm
tech.root: security
ms.assetid: 7da5f111-206d-40e1-9c40-4782118c3d49
ms.date: 12/05/2018
ms.keywords: GetCASetupProperty, GetCASetupProperty method [Security], GetCASetupProperty method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetCASetupProperty method, ICertSrvSetup.GetCASetupProperty, ICertSrvSetup::GetCASetupProperty, casetup/ICertSrvSetup::GetCASetupProperty, security.icertsrvsetup_getcasetupproperty
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
 - ICertSrvSetup::GetCASetupProperty
 - casetup/ICertSrvSetup::GetCASetupProperty
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
 - ICertSrvSetup.GetCASetupProperty
---

# ICertSrvSetup::GetCASetupProperty


## -description

The <b>GetCASetupProperty</b> method gets a property value for a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) configuration.

## -parameters

### -param propertyId [in]

A value of the <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a> enumeration that specifies the type of property to get.

### -param pPropertyValue [out]

A <b>VARIANT</b> value that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>