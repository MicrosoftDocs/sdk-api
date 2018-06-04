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

# WSManGetSessionOptionAsString function


## -description


Gets the value of a session option.


## -parameters




### -param session [in]

Specifies the session handle returned by a  <a href="https://msdn.microsoft.com/5123d876-5123-4fa4-8f6f-859a26aad825">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.


### -param option

Specifies the option to get. Not all session options can be retrieved. The values for the options are defined in the <a href="https://msdn.microsoft.com/6bfe6936-a9d2-4884-a354-41bd62a2feb0">WSManSessionOption</a> enumeration.


### -param stringLength

Specifies the length of the storage location for <i>string</i> parameter.


### -param string [out, optional]

A pointer to the storage location for the value of the specified session option.


### -param stringLengthUsed [out]

Specifies the length of the string returned in the <i>string</i> parameter.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.



