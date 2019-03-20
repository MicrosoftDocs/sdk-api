---
UID: NS:wsman._WSMAN_SELECTOR_SET
title: WSMAN_SELECTOR_SET (wsman.h)
author: windows-sdk-content
description: Defines a set of keys that represent the identity of a resource.
old-location: winrm\wsman_selector_set.htm
tech.root: winrm
ms.assetid: 8157c0e6-b992-46a9-9976-e57dd06e7f8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSMAN_SELECTOR_SET, WSMAN_SELECTOR_SET structure [Windows Remote Management], winrm.wsman_selector_set, wsman/WSMAN_SELECTOR_SET
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
 - WSMAN_SELECTOR_SET
product: Windows
targetos: Windows
req.typenames: WSMAN_SELECTOR_SET
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
---

# WSMAN_SELECTOR_SET structure


## -description


Defines a set of keys that represent the identity of a resource.


## -struct-fields




### -field numberKeys

Specifies the number of keys (selectors).


### -field keys

An array of <a href="https://msdn.microsoft.com/dbd66ad3-3816-43a3-a8e4-403ff3847da0">WSMAN_KEY</a>  structures that specify key names and values.

