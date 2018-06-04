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

# ASSOCKEY enumeration


## -description


Specifies the type of key to be returned by <a href="https://msdn.microsoft.com/7f380a9e-fda0-46be-88a1-fd73b0a4b7b7">IQueryAssociations::GetKey</a>.


## -enum-fields




### -field ASSOCKEY_SHELLEXECCLASS

A key that is passed to <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> through a <a href="https://msdn.microsoft.com/50e0dac3-b5dc-4d9f-8fd7-3a53a428166b">SHELLEXECUTEINFO</a> structure.


### -field ASSOCKEY_APP

An <b>Application</b> key for the file type.


### -field ASSOCKEY_CLASS

A ProgID or class key.


### -field ASSOCKEY_BASECLASS

A BaseClass value.


### -field ASSOCKEY_MAX



