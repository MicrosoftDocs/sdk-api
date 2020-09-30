---
UID: NF:casetup.IMSCEPSetup.GetMSCEPSetupProperty
title: IMSCEPSetup::GetMSCEPSetupProperty (casetup.h)
description: Gets a property value for a Network Device Enrollment Service (NDES) configuration.
helpviewer_keywords: ["GetMSCEPSetupProperty","GetMSCEPSetupProperty method [Security]","GetMSCEPSetupProperty method [Security]","IMSCEPSetup interface","IMSCEPSetup interface [Security]","GetMSCEPSetupProperty method","IMSCEPSetup.GetMSCEPSetupProperty","IMSCEPSetup::GetMSCEPSetupProperty","casetup/IMSCEPSetup::GetMSCEPSetupProperty","security.imscepsetup_getmscepsetupproperty"]
old-location: security\imscepsetup_getmscepsetupproperty.htm
tech.root: security
ms.assetid: b598331d-b54b-4e12-bea4-99cf1e6a5872
ms.date: 12/05/2018
ms.keywords: GetMSCEPSetupProperty, GetMSCEPSetupProperty method [Security], GetMSCEPSetupProperty method [Security],IMSCEPSetup interface, IMSCEPSetup interface [Security],GetMSCEPSetupProperty method, IMSCEPSetup.GetMSCEPSetupProperty, IMSCEPSetup::GetMSCEPSetupProperty, casetup/IMSCEPSetup::GetMSCEPSetupProperty, security.imscepsetup_getmscepsetupproperty
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
 - IMSCEPSetup::GetMSCEPSetupProperty
 - casetup/IMSCEPSetup::GetMSCEPSetupProperty
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
 - IMSCEPSetup.GetMSCEPSetupProperty
---

# IMSCEPSetup::GetMSCEPSetupProperty


## -description

The <b>GetMSCEPSetupProperty</b> method gets a property value for a Network Device Enrollment Service (NDES) configuration.

## -parameters

### -param propertyId [in]

A value of the <a href="/windows/win32/api/casetup/ne-casetup-mscepsetupproperty">MSCEPSetupProperty</a> enumeration that specifies the type of property to get.

### -param pVal [out]

A <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="/windows/win32/api/casetup/ne-casetup-mscepsetupproperty">MSCEPSetupProperty</a>.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>