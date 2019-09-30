---
UID: NE:intshcut.mimeassociationdialog_in_flags
title: MIMEASSOCIATIONDIALOG_IN_FLAGS (intshcut.h)
author: windows-sdk-content
description: Used with the MIMEAssociationDialog function to determine how it executes.
old-location: shell\MIMEASSOCIATIONDIALOG_IN_FLAGS.htm
tech.root: shell
ms.assetid: 916712a7-08ec-496d-aa83-42bf1e4bdbd8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MIMEASSOCDLG_FL_REGISTER_ASSOC, MIMEASSOCIATIONDIALOG_IN_FLAGS, MIMEASSOCIATIONDIALOG_IN_FLAGS enumeration [Windows Shell], _win32_MIMEASSOCIATIONDIALOG_IN_FLAGS, intshcut/MIMEASSOCDLG_FL_REGISTER_ASSOC, intshcut/MIMEASSOCIATIONDIALOG_IN_FLAGS, shell.MIMEASSOCIATIONDIALOG_IN_FLAGS
ms.topic: enum
f1_keywords: 
 - "intshcut/MIMEASSOCIATIONDIALOG_IN_FLAGS"
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intshcut.h
api_name:
 - MIMEASSOCIATIONDIALOG_IN_FLAGS
targetos: Windows
req.typenames: MIMEASSOCIATIONDIALOG_IN_FLAGS
req.redist: 
ms.custom: 19H1
---

# MIMEASSOCIATIONDIALOG_IN_FLAGS enumeration


## -description


Used with the <a href="https://docs.microsoft.com/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga">MIMEAssociationDialog</a> function to determine how it executes.


## -enum-fields




### -field MIMEASSOCDLG_FL_REGISTER_ASSOC

If this bit is set, the selected application is registered as the handler for the given MIME type. If this bit is clear, no association is registered.


## -remarks



An application is registered only if this flag is set and the user indicates that a persistent association is to be made.



