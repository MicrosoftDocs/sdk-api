---
UID: NE:intshcut.urlassociationdialog_in_flags
title: urlassociationdialog_in_flags
author: windows-sdk-content
description: The URLASSOCIATIONDIALOG_IN_FLAGS enumerated values are used with URLAssociationDialog to determine how it executes.
old-location: shell\URLASSOCIATIONDIALOG_IN_FLAGS.htm
old-project: shell
ms.assetid: bbfb0063-0d7e-432b-8428-a7652933c670
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: URLASSOCDLG_FL_REGISTER_ASSOC, URLASSOCDLG_FL_USE_DEFAULT_NAME, URLASSOCIATIONDIALOG_IN_FLAGS, URLASSOCIATIONDIALOG_IN_FLAGS enumeration [Windows Shell], _win32_URLASSOCIATIONDIALOG_IN_FLAGS, intshcut/URLASSOCDLG_FL_REGISTER_ASSOC, intshcut/URLASSOCDLG_FL_USE_DEFAULT_NAME, intshcut/URLASSOCIATIONDIALOG_IN_FLAGS, shell.URLASSOCIATIONDIALOG_IN_FLAGS, urlassociationdialog_in_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: intshcut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: URLASSOCIATIONDIALOG_IN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intshcut.h
api_name:
 - URLASSOCIATIONDIALOG_IN_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# urlassociationdialog_in_flags enumeration


## -description


The <b>URLASSOCIATIONDIALOG_IN_FLAGS</b> enumerated values are used with <a href="https://msdn.microsoft.com/3158e819-f131-4f57-8516-998955100377">URLAssociationDialog</a> to determine how it executes.


## -enum-fields




### -field URLASSOCDLG_FL_USE_DEFAULT_NAME

Use the default file name (that is, "Internet Shortcut").


### -field URLASSOCDLG_FL_REGISTER_ASSOC

Register the selected application as the handler for the protocol specified in the <i>pcszURL</i> parameter of <a href="https://msdn.microsoft.com/3158e819-f131-4f57-8516-998955100377">URLAssociationDialog</a>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.

