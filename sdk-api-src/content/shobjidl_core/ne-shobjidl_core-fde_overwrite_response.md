---
UID: NE:shobjidl_core.FDE_OVERWRITE_RESPONSE
title: FDE_OVERWRITE_RESPONSE (shobjidl_core.h)
description: Specifies the values used by the IFileDialogEvents::OnOverwrite method to indicate an application's response to an overwrite request during a save operation using the common file dialog.
helpviewer_keywords: ["FDEOR_ACCEPT","FDEOR_DEFAULT","FDEOR_REFUSE","FDE_OVERWRITE_RESPONSE","FDE_OVERWRITE_RESPONSE enumeration [Windows Shell]","shell.FDE_OVERWRITE_RESPONSE","shell_FDE_OVERWRITE_RESPONSE","shobjidl_core/FDEOR_ACCEPT","shobjidl_core/FDEOR_DEFAULT","shobjidl_core/FDEOR_REFUSE","shobjidl_core/FDE_OVERWRITE_RESPONSE"]
old-location: shell\FDE_OVERWRITE_RESPONSE.htm
tech.root: shell
ms.assetid: 2f278004-7f86-4b08-a724-bb95606c5d51
ms.date: 12/05/2018
ms.keywords: FDEOR_ACCEPT, FDEOR_DEFAULT, FDEOR_REFUSE, FDE_OVERWRITE_RESPONSE, FDE_OVERWRITE_RESPONSE enumeration [Windows Shell], shell.FDE_OVERWRITE_RESPONSE, shell_FDE_OVERWRITE_RESPONSE, shobjidl_core/FDEOR_ACCEPT, shobjidl_core/FDEOR_DEFAULT, shobjidl_core/FDEOR_REFUSE, shobjidl_core/FDE_OVERWRITE_RESPONSE
f1_keywords:
- shobjidl_core/FDE_OVERWRITE_RESPONSE
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
- shobjidl_core.h
api_name:
- FDE_OVERWRITE_RESPONSE
targetos: Windows
req.typenames: FDE_OVERWRITE_RESPONSE
req.redist: 
ms.custom: 19H1
---

# FDE_OVERWRITE_RESPONSE enumeration


## -description


Specifies the values used by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite">IFileDialogEvents::OnOverwrite</a> method to indicate an application's response to an overwrite request during a save operation using the common file dialog.


## -enum-fields




### -field FDEOR_DEFAULT

The application has not handled the event. The dialog displays a UI asking the user whether the file should be overwritten and returned from the dialog.


### -field FDEOR_ACCEPT

The application has determined that the file should be returned from the dialog.


### -field FDEOR_REFUSE

The application has determined that the file should not be returned from the dialog.

