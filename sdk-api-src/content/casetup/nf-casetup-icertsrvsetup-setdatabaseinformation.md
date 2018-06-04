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

# ICertSrvSetup::SetDatabaseInformation


## -description


The <b>SetDatabaseInformation</b> method sets the database related information for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) role.


## -parameters




### -param bstrDBDirectory [in]

A string that contains the name of the directory where the CA database files will be stored. This parameter must not be <b>NULL</b> or an empty string.


### -param bstrLogDirectory [in]

A string that contains the name of the directory where the CA database log files will be stored. This parameter must not be <b>NULL</b> or an empty string.


### -param bstrSharedFolder [in]

This parameter is reserved for future use and must be <b>NULL</b> or an empty string.


### -param bForceOverwrite [in]

A value that indicates whether to overwrite any existing database files in the specified directory. A value of <b>VARIANT_TRUE</b> specifies to overwrite existing files.


## -remarks



The <b>SetDatabaseInformation</b> method creates the specified directories if they do not exist.

Upon failure, the <b>SetDatabaseInformation</b> method might set additional error information in the <a href="https://msdn.microsoft.com/462fb4a6-2aad-46d4-98e0-32c095eff5c7">CAErrorId</a> and <a href="https://msdn.microsoft.com/154397f8-aa0e-4d74-b18e-b68b46fdfcdb">CAErrorString</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

