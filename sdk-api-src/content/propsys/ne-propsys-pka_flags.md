---
UID: NE:propsys.PKA_FLAGS
title: PKA_FLAGS (propsys.h)
description: Describes property change array behavior.
helpviewer_keywords: ["PKA_APPEND","PKA_DELETE","PKA_FLAGS","PKA_FLAGS enumeration [Windows Properties]","PKA_SET","_shell_PKA_FLAGS","properties.PKA_FLAGS","propsys/PKA_APPEND","propsys/PKA_DELETE","propsys/PKA_FLAGS","propsys/PKA_SET","shell.PKA_FLAGS"]
old-location: properties\PKA_FLAGS.htm
tech.root: properties
ms.assetid: 57cc5966-7983-4ecd-abee-36e5cc5401b6
ms.date: 12/05/2018
ms.keywords: PKA_APPEND, PKA_DELETE, PKA_FLAGS, PKA_FLAGS enumeration [Windows Properties], PKA_SET, _shell_PKA_FLAGS, properties.PKA_FLAGS, propsys/PKA_APPEND, propsys/PKA_DELETE, propsys/PKA_FLAGS, propsys/PKA_SET, shell.PKA_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PKA_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PKA_FLAGS
 - propsys/PKA_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propsys.h
api_name:
 - PKA_FLAGS
---

# PKA_FLAGS enumeration


## -description

Describes property change array behavior.

## -enum-fields

### -field PKA_SET:0

Replace current value.

### -field PKA_APPEND

Append to current value - multi-value properties only.

### -field PKA_DELETE

Delete from current value - multi-value properties only.

