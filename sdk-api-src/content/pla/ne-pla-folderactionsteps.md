---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0012
title: FolderActionSteps (pla.h)
description: Defines the action that the data manager takes when both the age and size limits are met.
helpviewer_keywords: ["FolderActionSteps","FolderActionSteps enumeration [PLA]","__MIDL___MIDL_itf_pla_0001_0043_0012","base.folderactionsteps","pla.folderactionsteps","pla/FolderActionSteps","pla/plaCreateCab","pla/plaDeleteCab","pla/plaDeleteData","pla/plaDeleteReport","pla/plaSendCab","plaCreateCab","plaDeleteCab","plaDeleteData","plaDeleteReport","plaSendCab"]
old-location: pla\folderactionsteps.htm
tech.root: PLA
ms.assetid: 94d199a1-36f7-4064-a4fb-90dd26c37960
ms.date: 12/05/2018
ms.keywords: FolderActionSteps, FolderActionSteps enumeration [PLA], __MIDL___MIDL_itf_pla_0001_0043_0012, base.folderactionsteps, pla.folderactionsteps, pla/FolderActionSteps, pla/plaCreateCab, pla/plaDeleteCab, pla/plaDeleteData, pla/plaDeleteReport, pla/plaSendCab, plaCreateCab, plaDeleteCab, plaDeleteData, plaDeleteReport, plaSendCab
req.header: pla.h
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
req.typenames: FolderActionSteps
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0012
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0012
 - FolderActionSteps
 - pla/FolderActionSteps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - FolderActionSteps
---

# FolderActionSteps enumeration


## -description

Defines the action that the data manager takes when both the age and size limits are met.

## -enum-fields

### -field plaCreateCab:0x1

Creates a cabinet file. The name of the cabinet file is  <i>nameofthesubfolder</i>.cab.

### -field plaDeleteData:0x2

Deletes all files in the folder, except the report and cabinet file.

### -field plaSendCab:0x4

Sends the cabinet file to the location specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ifolderaction-get_sendcabto">IFolderAction::SendCabTo</a> property.

### -field plaDeleteCab:0x8

Deletes the cabinet file.

### -field plaDeleteReport:0x10

Deletes the report file.

## -remarks

Specify one or more actions. The data manager applies the actions in the order in which they are defined in this enumeration.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-ifolderaction-get_actions">IFolderAction::Actions</a>
