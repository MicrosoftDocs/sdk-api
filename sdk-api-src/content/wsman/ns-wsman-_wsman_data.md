---
UID: NS:wsman._WSMAN_DATA
title: "_WSMAN_DATA"
author: windows-sdk-content
description: Contains inbound and outbound data used in the Windows Remote Management (WinRM) API.
old-location: winrm\wsman_data.htm
old-project: WinRM
ms.assetid: 4ff574d4-04b0-47c3-808f-867d6815bffc
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSMAN_DATA, WSMAN_DATA structure [Windows Remote Management], _WSMAN_DATA, winrm.wsman_data, wsman/WSMAN_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsman.h
req.include-header: 
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
req.typenames: WSMAN_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsman.h
api_name:
-	WSMAN_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_DATA structure


## -description


Contains inbound and outbound data used in the Windows Remote Management (WinRM) API.


## -struct-fields




### -field type

Specifies the type of data currently stored in the union.


### -field text

 


### -field binaryData

 


### -field number

 




#### - ( unnamed union )

Contains the data.



#### text

If <b>type</b> is <b>WSMAN_DATA_TYPE_TEXT</b>,  <b>text</b> contains a <a href="https://msdn.microsoft.com/463dcc6a-2a56-42a9-a778-7a634e5f977c">WSMAN_DATA_TEXT</a> structure.



#### binaryData

If <b>type</b> is <b>WSMAN_DATA_TYPE_XML_BINARY</b>, <b>binaryData</b> contains a <a href="https://msdn.microsoft.com/35beedc3-30c6-4e04-bc27-bb9eb21256fe">WSMAN_DATA_BINARY</a> structure.



#### number

If <b>type</b> is <b>WSMAN_DATA_TYPE_DWORD</b>, <b>number</b> is a DWORD integer.

