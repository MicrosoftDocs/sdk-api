---
UID: NF:casetup.ICertSrvSetup.SetCASetupProperty
title: ICertSrvSetup::SetCASetupProperty
author: windows-sdk-content
description: Sets a property value for a certification authority (CA) configuration.
old-location: security\icertsrvsetup_setcasetupproperty.htm
tech.root: seccrypto
ms.assetid: 91df1926-a4b6-4ba2-ab59-0258293fc1c0
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ICertSrvSetup interface [Security],SetCASetupProperty method, ICertSrvSetup.SetCASetupProperty, ICertSrvSetup::SetCASetupProperty, SetCASetupProperty, SetCASetupProperty method [Security], SetCASetupProperty method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetCASetupProperty, security.icertsrvsetup_setcasetupproperty
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
 - ICertSrvSetup.SetCASetupProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertSrvSetup::SetCASetupProperty


## -description


The <b>SetCASetupProperty</b> method sets a property value for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA) configuration.


## -parameters




### -param propertyId [in]

A <a href="https://msdn.microsoft.com/en-us/library/Bb648668(v=VS.85).aspx">CASetupProperty</a> constant that specifies the type of property to configure.

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

A pointer to a <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/en-us/library/Bb648668(v=VS.85).aspx">CASetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb736371(v=VS.85).aspx">ICertSrvSetup</a>
 

 

