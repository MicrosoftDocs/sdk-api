---
UID: NF:casetup.IMSCEPSetup.SetMSCEPSetupProperty
title: IMSCEPSetup::SetMSCEPSetupProperty (casetup.h)
author: windows-sdk-content
description: Sets a property value for a Network Device Enrollment Service (NDES) configuration.
old-location: security\imscepsetup_setmscepsetupproperty.htm
tech.root: SecCrypto
ms.assetid: 868f3e5f-1345-414b-a75f-d2e68213469b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSCEPSetup interface [Security],SetMSCEPSetupProperty method, IMSCEPSetup.SetMSCEPSetupProperty, IMSCEPSetup::SetMSCEPSetupProperty, SetMSCEPSetupProperty, SetMSCEPSetupProperty method [Security], SetMSCEPSetupProperty method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::SetMSCEPSetupProperty, security.imscepsetup_setmscepsetupproperty
ms.topic: method
f1_keywords: ["casetup/IMSCEPSetup.SetMSCEPSetupProperty"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - IMSCEPSetup.SetMSCEPSetupProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSCEPSetup::SetMSCEPSetupProperty


## -description


The <b>SetMSCEPSetupProperty</b> method sets a property value for a Network Device Enrollment Service (NDES) configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/casetup/ne-casetup-__midl___midl_itf_casetup_0000_0003_0001">MSCEPSetupProperty</a> enumeration that specifies the type of property to configure.


### -param pPropertyValue [in]

A pointer to a  <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://docs.microsoft.com/windows/desktop/api/casetup/ne-casetup-__midl___midl_itf_casetup_0000_0003_0001">MSCEPSetupProperty</a>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/casetup/nn-casetup-imscepsetup">IMSCEPSetup</a>
 

 

