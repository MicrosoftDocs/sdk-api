---
UID: NS:wsman._WSMAN_OPERATION_INFO
title: "_WSMAN_OPERATION_INFO"
author: windows-sdk-content
description: Represents a specific resource endpoint for which the plug-in must perform the request.
old-location: winrm\wsman_operation_info.htm
old-project: winrm
ms.assetid: a73029c6-d4e7-4cb3-ad0a-b71baffdbeb6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSMAN_OPERATION_INFO, WSMAN_OPERATION_INFO structure [Windows Remote Management], _WSMAN_OPERATION_INFO, winrm.wsman_operation_info, wsman/WSMAN_OPERATION_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSMAN_OPERATION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_OPERATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_OPERATION_INFO structure


## -description


Represents a specific resource endpoint for which the plug-in must perform the request.


## -struct-fields




### -field fragment

A <a href="https://msdn.microsoft.com/2aa4ee38-6991-4f95-90fd-867b188fc9ff">WSMAN_FRAGMENT</a> structure that specifies the subset of data to be used for the operation. This parameter is reserved for future use and is ignored on receipt.


### -field filter

A <a href="https://msdn.microsoft.com/d99c11a8-e91f-428f-98b1-d3116d027691">WSMAN_FILTER</a> structure that specifies the filtering that is used for the operation. This parameter is reserved for future use and is ignored on receipt.


### -field selectorSet

A <a href="https://msdn.microsoft.com/8157c0e6-b992-46a9-9976-e57dd06e7f8b">WSMAN_SELECTOR_SET</a> structure that identifies the specific resource to use for the request.


### -field optionSet

A <a href="https://msdn.microsoft.com/16a1447c-d764-44bf-9c62-064769ead0f3">WSMAN_OPTION_SET</a> structure that specifies the set of options for the request.


### -field reserved

 


### -field version

 



