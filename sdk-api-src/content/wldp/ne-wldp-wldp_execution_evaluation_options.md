---
UID: NE:wldp.WLDP_EXECUTION_EVALUATION_OPTIONS
tech.root: security
title: WLDP_EXECUTION_EVALUATION_OPTIONS
ms.date: 08/23/2022
targetos: Windows
description: Specifies execution options when querying for execution authorization with WldpCanExecuteBuffer, WldpCanExecuteFile, and WldpCanExecuteStream.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wldp.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11, Build 22621
req.target-min-winversvr: Windows 11, Build 22621
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wldp.h
api_name:
 - WLDP_EXECUTION_EVALUATION_OPTIONS
f1_keywords:
 - WLDP_EXECUTION_EVALUATION_OPTIONS
 - wldp/WLDP_EXECUTION_EVALUATION_OPTIONS
dev_langs:
 - c++
helpviewer_keywords:
 - WLDP_EXECUTION_EVALUATION_OPTIONS
---

## -description

Specifies execution options when querying for execution authorization with [WldpCanExecuteBuffer](nf-wldp-wldpcanexecutebuffer.md), [WldpCanExecuteFile](nf-wldp-wldpcanexecutefile.md), and [WldpCanExecuteStream](nf-wldp-wldpcanexecutestream.md).

## -enum-fields

### -field WLDP_EXECUTION_EVALUATION_OPTION_NONE

No options.

### -field WLDP_EXECUTION_EVALUATION_OPTION_EXECUTE_IN_INTERACTIVE_SESSION

The execution is requested for an interactive session, such as using Powershell or cmd.

## -remarks

## -see-also

