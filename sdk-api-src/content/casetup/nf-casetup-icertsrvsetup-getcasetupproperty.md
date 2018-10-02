---
UID: NF:casetup.ICertSrvSetup.GetCASetupProperty
title: ICertSrvSetup::GetCASetupProperty
author: windows-sdk-content
description: Gets a property value for a certification authority (CA) configuration.
old-location: security\icertsrvsetup_getcasetupproperty.htm
tech.root: seccrypto
ms.assetid: 7da5f111-206d-40e1-9c40-4782118c3d49
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: GetCASetupProperty, GetCASetupProperty method [Security], GetCASetupProperty method [Security],ICertSrvSetup interface, ICertSrvSetup interface [Security],GetCASetupProperty method, ICertSrvSetup.GetCASetupProperty, ICertSrvSetup::GetCASetupProperty, casetup/ICertSrvSetup::GetCASetupProperty, security.icertsrvsetup_getcasetupproperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertSrvSetup.GetCASetupProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::GetCASetupProperty


## -description


The <b>GetCASetupProperty</b> method gets a property value for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) configuration.


## -parameters




### -param propertyId [in]

A value of the <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a> enumeration that specifies the type of property to get.


### -param pPropertyValue [out]

A <b>VARIANT</b> value that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

