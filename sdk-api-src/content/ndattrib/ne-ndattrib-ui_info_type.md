---
UID: NE:ndattrib.__MIDL___MIDL_itf_ndattrib_0000_0000_0003
title: UI_INFO_TYPE (ndattrib.h)
description: The UI_INFO_TYPE enumeration identifies repairs that perform user interface tasks.
helpviewer_keywords: ["UIT_DUI","UIT_HELP_PANE","UIT_NONE","UIT_SHELL_COMMAND","UI_INFO_TYPE","UI_INFO_TYPE enumeration [NDF]","ndattrib/UIT_DUI","ndattrib/UIT_HELP_PANE","ndattrib/UIT_NONE","ndattrib/UIT_SHELL_COMMAND","ndattrib/UI_INFO_TYPE","ndf.ui_info_type"]
old-location: ndf\ui_info_type.htm
tech.root: NDF
ms.assetid: 819ab594-860b-42a0-be6e-bab0e669c200
ms.date: 12/05/2018
ms.keywords: UIT_DUI, UIT_HELP_PANE, UIT_NONE, UIT_SHELL_COMMAND, UI_INFO_TYPE, UI_INFO_TYPE enumeration [NDF], ndattrib/UIT_DUI, ndattrib/UIT_HELP_PANE, ndattrib/UIT_NONE, ndattrib/UIT_SHELL_COMMAND, ndattrib/UI_INFO_TYPE, ndf.ui_info_type
req.header: ndattrib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
targetos: Windows
req.typenames: UI_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ndattrib_0000_0000_0003
 - ndattrib/__MIDL___MIDL_itf_ndattrib_0000_0000_0003
 - UI_INFO_TYPE
 - ndattrib/UI_INFO_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ndattrib.h
api_name:
 - UI_INFO_TYPE
---

# UI_INFO_TYPE enumeration


## -description

The <b>UI_INFO_TYPE</b> enumeration identifies repairs that perform user interface tasks.

## -enum-fields

### -field UIT_INVALID:0

### -field UIT_NONE:1

No additional repair interfaces are present.

### -field UIT_SHELL_COMMAND

Execute shell command.

### -field UIT_HELP_PANE

Launch help pane.

### -field UIT_DUI

Direct UI.

