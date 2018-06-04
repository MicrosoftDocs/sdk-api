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

# _SAFER_PATHNAME_IDENTIFICATION structure


## -description


The <b>SAFER_PATHNAME_IDENTIFICATION</b> structure represents a path identification rule.


## -struct-fields




### -field header

A  <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure containing the structure header. The <b>dwIdentificationType</b> member of the header must be <b>SaferIdentityTypeImageName</b>, and the  <b>cbStructSize</b> member of the header must be sizeof(SAFER_PATHNAME_IDENTIFICATION).


### -field Description

A description of the path identification rule provided by the user.


### -field ImageName

A pointer to a <b>null</b>-terminated wide character string that specifies the fully qualified path and file name to be used for path-based discrimination checks. The image name is also used to open and read the file to identify any other discrimination criteria not supplied in this structure. This member can be set to <b>NULL</b>. If the <b>dwCheckFlags</b> member of the <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure specified by the <b>header</b> member includes SAFER_CRITERIA_AUTHENTICODE, either the <b>hImageFileHandle</b> member or the <b>ImagePath</b> member of the <b>SAFER_IDENTIFICATION_HEADER</b> structure must be set.


### -field dwSaferFlags

Reserved for future use.

