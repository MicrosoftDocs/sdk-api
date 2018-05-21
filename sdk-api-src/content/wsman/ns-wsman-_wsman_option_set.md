---
UID: NS:wsman._WSMAN_OPTION_SET
title: "_WSMAN_OPTION_SET"
author: windows-driver-content
description: Represents a set of options.
old-location: winrm\wsman_option_set.htm
old-project: WinRM
ms.assetid: 16a1447c-d764-44bf-9c62-064769ead0f3
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSMAN_OPTION_SET, WSMAN_OPTION_SET structure [Windows Remote Management], _WSMAN_OPTION_SET, winrm.wsman_option_set, wsman/WSMAN_OPTION_SET
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WSMAN_OPTION_SET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wsman.h
api_name:
-	WSMAN_OPTION_SET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSMAN_OPTION_SET structure


## -description


Represents a set of options. Additionally, this structure defines  a flag that specifies whether all options must be understood.


## -struct-fields




### -field optionsCount

Specifies the number of options in the <b>options</b> array.


### -field options

Specifies an array of option names and values


### -field optionsMustUnderstand

If this member is <b>TRUE</b>, the plug-in must return an error if any of the options are not understood.

