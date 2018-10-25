---
UID: NF:casetup.IMSCEPSetup.SetMSCEPSetupProperty
title: IMSCEPSetup::SetMSCEPSetupProperty
author: windows-sdk-content
description: Sets a property value for a Network Device Enrollment Service (NDES) configuration.
old-location: security\imscepsetup_setmscepsetupproperty.htm
tech.root: seccrypto
ms.assetid: 868f3e5f-1345-414b-a75f-d2e68213469b
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: IMSCEPSetup interface [Security],SetMSCEPSetupProperty method, IMSCEPSetup.SetMSCEPSetupProperty, IMSCEPSetup::SetMSCEPSetupProperty, SetMSCEPSetupProperty, SetMSCEPSetupProperty method [Security], SetMSCEPSetupProperty method [Security],IMSCEPSetup interface, casetup/IMSCEPSetup::SetMSCEPSetupProperty, security.imscepsetup_setmscepsetupproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IMSCEPSetup::SetMSCEPSetupProperty


## -description


The <b>SetMSCEPSetupProperty</b> method sets a property value for a Network Device Enrollment Service (NDES) configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a> enumeration that specifies the type of property to configure.


### -param pPropertyValue [in]

A pointer to a  <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>
 

 

