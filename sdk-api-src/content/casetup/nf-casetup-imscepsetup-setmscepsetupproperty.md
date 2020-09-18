---
UID: NF:casetup.IMSCEPSetup.SetMSCEPSetupProperty
title: IMSCEPSetup::SetMSCEPSetupProperty (casetup.h)
description: Sets a property value for a Network Device Enrollment Service (NDES) configuration.
helpviewer_keywords: ["IMSCEPSetup interface [Security]","SetMSCEPSetupProperty method","IMSCEPSetup.SetMSCEPSetupProperty","IMSCEPSetup::SetMSCEPSetupProperty","SetMSCEPSetupProperty","SetMSCEPSetupProperty method [Security]","SetMSCEPSetupProperty method [Security]","IMSCEPSetup interface","casetup/IMSCEPSetup::SetMSCEPSetupProperty","security.imscepsetup_setmscepsetupproperty"]
old-location: security\imscepsetup_setmscepsetupproperty.htm
tech.root: security
ms.assetid: 868f3e5f-1345-414b-a75f-d2e68213469b
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup interface [Security],SetMSCEPSetupProperty method, IMSCEPSetup.SetMSCEPSetupProperty, IMSCEPSetup::SetMSCEPSetupProperty, SetMSCEPSetupProperty, SetMSCEPSetupProperty method [Security], SetMSCEPSetupProperty method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::SetMSCEPSetupProperty, security.imscepsetup_setmscepsetupproperty
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
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
 - IMSCEPSetup::SetMSCEPSetupProperty
 - casetup/IMSCEPSetup::SetMSCEPSetupProperty
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
 - IMSCEPSetup.SetMSCEPSetupProperty
---

# IMSCEPSetup::SetMSCEPSetupProperty


## -description

The <b>SetMSCEPSetupProperty</b> method sets a property value for a Network Device Enrollment Service (NDES) configuration.

## -parameters

### -param propertyId [in]

A value of the <a href="/windows/win32/api/casetup/ne-casetup-mscepsetupproperty">MSCEPSetupProperty</a> enumeration that specifies the type of property to configure.

### -param pPropertyValue [in]

A pointer to a  <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="/windows/win32/api/casetup/ne-casetup-mscepsetupproperty">MSCEPSetupProperty</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>