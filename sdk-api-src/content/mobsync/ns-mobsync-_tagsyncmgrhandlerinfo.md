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

# _tagSYNCMGRHANDLERINFO structure


## -description


Provides information about the handler for use in the <a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">ISyncMgrSynchronize::GetHandlerInfo</a> method.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure in bytes.


### -field hIcon

Type: <b>HICON</b>

The icon for the handler.


### -field SyncMgrHandlerFlags

Type: <b>DWORD</b>

The value of the <a href="https://msdn.microsoft.com/9e5f7f49-f2f0-4fa3-8822-8e6074cd4f47">SYNCMGRHANDLERFLAGS</a> enumeration.


### -field wszHandlerName

Type: <b>WCHAR[MAX_SYNCMGRHANDLERNAME]</b>

The name to use for the handler.


## -see-also




<a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">ISyncMgrSynchronize::GetHandlerInfo</a>



<a href="https://msdn.microsoft.com/9e5f7f49-f2f0-4fa3-8822-8e6074cd4f47">SYNCMGRHANDLERFLAGS</a>
 

 

