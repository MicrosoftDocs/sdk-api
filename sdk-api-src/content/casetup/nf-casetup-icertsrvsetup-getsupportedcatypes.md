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

# ICertSrvSetup::GetSupportedCATypes


## -description


The <b>GetSupportedCATypes</b> method gets the types of <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authorities</a> (CAs) that can be installed on a computer under the caller context. This method does not change the state of the <b>CCertSrvSetup</b> object.


## -parameters




### -param pCATypes [out]

A pointer to a <b>VARIANT</b> array of <b>VT_UI4</b> types that specify the supported CAs. The <a href="https://msdn.microsoft.com/32b20317-c0ef-4896-a8c6-309e34f87c30">ENUM_CATYPES</a> enumeration specifies the possible values for the array.


## -see-also




<a href="https://msdn.microsoft.com/6792a0d6-d304-481d-a97b-5fb7033c7eae">ICertSrvSetup</a>
 

 

