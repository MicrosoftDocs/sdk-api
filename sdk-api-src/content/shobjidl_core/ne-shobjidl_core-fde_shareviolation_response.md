---
UID: NE:shobjidl_core.FDE_SHAREVIOLATION_RESPONSE
title: FDE_SHAREVIOLATION_RESPONSE
author: windows-sdk-content
description: Specifies the values used by the IFileDialogEvents::OnShareViolation method to indicate an application's response to a sharing violation that occurs when a file is opened or saved.
old-location: shell\FDE_SHAREVIOLATION_RESPONSE.htm
tech.root: shell
ms.assetid: 976965f5-7806-41de-b1d4-f5bb6dc4f79b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FDESVR_ACCEPT, FDESVR_DEFAULT, FDESVR_REFUSE, FDE_SHAREVIOLATION_RESPONSE, FDE_SHAREVIOLATION_RESPONSE enumeration [Windows Shell], shell.FDE_SHAREVIOLATION_RESPONSE, shell_FDE_SHAREVIOLATION_RESPONSE, shobjidl_core/FDESVR_ACCEPT, shobjidl_core/FDESVR_DEFAULT, shobjidl_core/FDESVR_REFUSE, shobjidl_core/FDE_SHAREVIOLATION_RESPONSE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - FDE_SHAREVIOLATION_RESPONSE
product: Windows
targetos: Windows
req.typenames: FDE_SHAREVIOLATION_RESPONSE
req.redist: 
---

# FDE_SHAREVIOLATION_RESPONSE enumeration


## -description


Specifies the values used by the <a href="https://msdn.microsoft.com/bd9cfa69-4e55-48ca-915a-e5ecccf8bf96">IFileDialogEvents::OnShareViolation</a> method to indicate an application's response to a sharing violation that occurs when a file is opened or saved.


## -enum-fields




### -field FDESVR_DEFAULT

The application has not handled the event. The dialog displays a UI that indicates that the file is in use and a different file must be chosen.


### -field FDESVR_ACCEPT

The application has determined that the file should be returned from the dialog.


### -field FDESVR_REFUSE

The application has determined that the file should not be returned from the dialog.

