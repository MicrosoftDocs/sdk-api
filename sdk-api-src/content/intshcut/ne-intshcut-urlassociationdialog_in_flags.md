---
UID: NE:intshcut.urlassociationdialog_in_flags
title: URLASSOCIATIONDIALOG_IN_FLAGS (intshcut.h)
description: The URLASSOCIATIONDIALOG_IN_FLAGS enumerated values are used with URLAssociationDialog to determine how it executes.
helpviewer_keywords: ["URLASSOCDLG_FL_REGISTER_ASSOC","URLASSOCDLG_FL_USE_DEFAULT_NAME","URLASSOCIATIONDIALOG_IN_FLAGS","URLASSOCIATIONDIALOG_IN_FLAGS enumeration [Windows Shell]","_win32_URLASSOCIATIONDIALOG_IN_FLAGS","intshcut/URLASSOCDLG_FL_REGISTER_ASSOC","intshcut/URLASSOCDLG_FL_USE_DEFAULT_NAME","intshcut/URLASSOCIATIONDIALOG_IN_FLAGS","shell.URLASSOCIATIONDIALOG_IN_FLAGS"]
old-location: shell\URLASSOCIATIONDIALOG_IN_FLAGS.htm
tech.root: shell
ms.assetid: bbfb0063-0d7e-432b-8428-a7652933c670
ms.date: 12/05/2018
ms.keywords: URLASSOCDLG_FL_REGISTER_ASSOC, URLASSOCDLG_FL_USE_DEFAULT_NAME, URLASSOCIATIONDIALOG_IN_FLAGS, URLASSOCIATIONDIALOG_IN_FLAGS enumeration [Windows Shell], _win32_URLASSOCIATIONDIALOG_IN_FLAGS, intshcut/URLASSOCDLG_FL_REGISTER_ASSOC, intshcut/URLASSOCDLG_FL_USE_DEFAULT_NAME, intshcut/URLASSOCIATIONDIALOG_IN_FLAGS, shell.URLASSOCIATIONDIALOG_IN_FLAGS
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
targetos: Windows
req.typenames: URLASSOCIATIONDIALOG_IN_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - urlassociationdialog_in_flags
 - intshcut/urlassociationdialog_in_flags
 - URLASSOCIATIONDIALOG_IN_FLAGS
 - intshcut/URLASSOCIATIONDIALOG_IN_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intshcut.h
api_name:
 - URLASSOCIATIONDIALOG_IN_FLAGS
---

# URLASSOCIATIONDIALOG_IN_FLAGS enumeration


## -description

The <b>URLASSOCIATIONDIALOG_IN_FLAGS</b> enumerated values are used with <a href="/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga">URLAssociationDialog</a> to determine how it executes.

## -enum-fields

### -field URLASSOCDLG_FL_USE_DEFAULT_NAME:0x0001

Use the default file name (that is, "Internet Shortcut").

### -field URLASSOCDLG_FL_REGISTER_ASSOC:0x0002

Register the selected application as the handler for the protocol specified in the <i>pcszURL</i> parameter of <a href="/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga">URLAssociationDialog</a>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.
