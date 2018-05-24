---
UID: NE:propsys.PSC_STATE
title: PSC_STATE
author: windows-driver-content
description: Specifies the state of a property. They are set manually by the code that is hosting the in-memory property store cache.
old-location: properties\PSC_STATE.htm
old-project: properties
ms.assetid: f6a09b32-e642-4c11-ae89-fed787b4913c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: PSC_DIRTY, PSC_NORMAL, PSC_NOTINSOURCE, PSC_STATE, PSC_STATE enumeration [Windows Properties], properties.PSC_STATE, propsys/PSC_DIRTY, propsys/PSC_NORMAL, propsys/PSC_NOTINSOURCE, propsys/PSC_STATE, shell.PSC_STATE, shell_PSC_STATE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Propsys.h
api_name:
-	PSC_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PSC_STATE enumeration


## -description


Specifies the state of a property. They are set manually by the code that is hosting the in-memory property store cache.


## -enum-fields




### -field PSC_NORMAL

The property has not been altered.


### -field PSC_NOTINSOURCE

The requested property does not exist for the file or stream on which the property handler was initialized.


### -field PSC_DIRTY

The property has been altered but has not yet been committed to the file or stream.


### -field PSC_READONLY



