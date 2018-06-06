---
UID: NS:winternl._STRING
title: "_STRING"
author: windows-sdk-content
description: Used with the RtlUnicodeStringToOemString function.
old-location: winprog\_win32_string.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\misc\string.htm
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: "*PSTRING, ANSI_STRING, OEM_STRING, OEM_STRING structure [Windows API], PSTRING, PSTRING structure pointer [Windows API], STRING, STRING structure [Windows API], _STRING, _win32_STRING, winprog._win32_string, winternl/OEM_STRING, winternl/PSTRING, winternl/STRING, winui._win32_string"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: STRING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - STRING
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _STRING structure


## -description


Used with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553255">RtlUnicodeStringToOemString</a> function. 


## -struct-fields




### -field Length

The length of the buffer.


### -field MaximumLength

The maximum length of the buffer.


### -field Buffer

The address of the buffer.


## -remarks



The data type used in the <b>DestinationString</b> parameter of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553255">RtlUnicodeStringToOemString</a> function, <code> POEM_STRING</code>, is defined as:
		
                

<code>typedef PSTRING POEM_STRING;</code>



