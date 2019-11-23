---
UID: NS:wsman._WSMAN_OPTION_SET
title: WSMAN_OPTION_SET (wsman.h)

description: Represents a set of options.
old-location: winrm\wsman_option_set.htm
tech.root: winrm
ms.assetid: 16a1447c-d764-44bf-9c62-064769ead0f3

ms.date: 12/05/2018
ms.keywords: WSMAN_OPTION_SET, WSMAN_OPTION_SET structure [Windows Remote Management], winrm.wsman_option_set, wsman/WSMAN_OPTION_SET
ms.topic: struct
f1_keywords: 
 - "wsman/WSMAN_OPTION_SET"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_OPTION_SET
targetos: Windows
req.typenames: WSMAN_OPTION_SET
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
---

# WSMAN_OPTION_SET structure


## -description


Represents a set of options. Additionally, this structure defines  a flag that specifies whether all options must be understood.


## -struct-fields




### -field optionsCount

Specifies the number of options in the <b>options</b> array.


### -field options

Specifies an array of option names and values


### -field optionsMustUnderstand

If this member is <b>TRUE</b>, the plug-in must return an error if any of the options are not understood.

