---
UID: NF:casetup.IMSCEPSetup.GetMSCEPSetupProperty
title: IMSCEPSetup::GetMSCEPSetupProperty
author: windows-sdk-content
description: Gets a property value for a Network Device Enrollment Service (NDES) configuration.
old-location: security\imscepsetup_getmscepsetupproperty.htm
tech.root: seccrypto
ms.assetid: b598331d-b54b-4e12-bea4-99cf1e6a5872
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetMSCEPSetupProperty, GetMSCEPSetupProperty method [Security], GetMSCEPSetupProperty method [Security],IMSCEPSetup interface, IMSCEPSetup interface [Security],GetMSCEPSetupProperty method, IMSCEPSetup.GetMSCEPSetupProperty, IMSCEPSetup::GetMSCEPSetupProperty, casetup/IMSCEPSetup::GetMSCEPSetupProperty, security.imscepsetup_getmscepsetupproperty
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
 - IMSCEPSetup.GetMSCEPSetupProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSCEPSetup::GetMSCEPSetupProperty


## -description


The <b>GetMSCEPSetupProperty</b> method gets a property value for a Network Device Enrollment Service (NDES) configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a> enumeration that specifies the type of property to get.


### -param pVal [out]

A <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/c3740afc-842e-427f-87bf-022f5544d0d4">MSCEPSetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/328c6c04-7ade-4b64-bd8a-4314b6e8dc78">IMSCEPSetup</a>
 

 

