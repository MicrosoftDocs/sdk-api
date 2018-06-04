---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICertSrvSetup::SetCASetupProperty


## -description


The <b>SetCASetupProperty</b> method sets a property value for a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) configuration.


## -parameters




### -param propertyId [in]

A <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a> constant that specifies the type of property to configure.

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

A pointer to a <b>VARIANT</b> that specifies the property value. The <b>VARIANT</b> type depends on the property type. For more information about the <b>VARIANT</b> type, see <a href="https://msdn.microsoft.com/2245ad2f-89ca-4478-91d0-cbd7a0648479">CASetupProperty</a>.


## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

