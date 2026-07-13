---
UID: NS:shdeprecated.tagFolderSetData
title: FOLDERSETDATA (shdeprecated.h)
description: Deprecated. Data used in IBrowserService2::GetFolderSetData.
helpviewer_keywords: ["*LPFOLDERSETDATA","FOLDERSETDATA","FOLDERSETDATA structure [Windows Shell]","LPFOLDERSETDATA","LPFOLDERSETDATA structure pointer [Windows Shell]","VIEW_PRIORITY_CACHEHIT","VIEW_PRIORITY_CACHEMISS","VIEW_PRIORITY_DESPERATE","VIEW_PRIORITY_INHERIT","VIEW_PRIORITY_NONE","VIEW_PRIORITY_RESTRICTED","VIEW_PRIORITY_SHELLEXT","VIEW_PRIORITY_SHELLEXT_ASBACKUP","VIEW_PRIORITY_STALECACHEHIT","VIEW_PRIORITY_USEASDEFAULT","_shell_FOLDERSETDATA","shdeprecated/FOLDERSETDATA","shdeprecated/LPFOLDERSETDATA","shell.FOLDERSETDATA"]
old-location: shell\FOLDERSETDATA.htm
tech.root: shell
ms.assetid: eb47cd77-5788-4130-8d9c-cc84582e5d8e
ms.date: 12/05/2018
ms.keywords: '*LPFOLDERSETDATA, FOLDERSETDATA, FOLDERSETDATA structure [Windows Shell], LPFOLDERSETDATA, LPFOLDERSETDATA structure pointer [Windows Shell], VIEW_PRIORITY_CACHEHIT, VIEW_PRIORITY_CACHEMISS, VIEW_PRIORITY_DESPERATE, VIEW_PRIORITY_INHERIT, VIEW_PRIORITY_NONE, VIEW_PRIORITY_RESTRICTED, VIEW_PRIORITY_SHELLEXT, VIEW_PRIORITY_SHELLEXT_ASBACKUP, VIEW_PRIORITY_STALECACHEHIT, VIEW_PRIORITY_USEASDEFAULT, _shell_FOLDERSETDATA, shdeprecated/FOLDERSETDATA, shdeprecated/LPFOLDERSETDATA, shell.FOLDERSETDATA'
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FOLDERSETDATA, *LPFOLDERSETDATA
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - tagFolderSetData
 - shdeprecated/tagFolderSetData
 - LPFOLDERSETDATA
 - shdeprecated/LPFOLDERSETDATA
 - FOLDERSETDATA
 - shdeprecated/FOLDERSETDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shdeprecated.h
api_name:
 - FOLDERSETDATA
---

# FOLDERSETDATA structure


## -description

<p class="CCE_Message">[<b>FOLDERSETDATA</b> may be altered or unavailable in subsequent versions of the operating system or product.]

Deprecated. Data used in <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-getfoldersetdata">IBrowserService2::GetFolderSetData</a>.

## -struct-fields

### -field _fs

Type: <b><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a></b>

The <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings">FOLDERSETTINGS</a> structure containing folder view information.

### -field _vidRestore

Type: <b>SHELLVIEWID</b>

The last view used for this folder, used as a suggestion for this visit.

### -field _dwViewPriority

Type: <b>DWORD</b>

One of the following values indicating the priority used in choosing the view, listed from highest priority to lowest.



#### VIEW_PRIORITY_RESTRICTED

A Shell restriction is in place that forces this view to be used.



#### VIEW_PRIORITY_CACHEHIT

Current information for this view stored in the registry should be used.



#### VIEW_PRIORITY_STALECACHEHIT

Stored registry information for this view is out of date, so the default view for folders of this type should be used.



#### VIEW_PRIORITY_USEASDEFAULT

The default view for folders of this type should be used.



#### VIEW_PRIORITY_SHELLEXT

The Shell extension determines which view should be used.



#### VIEW_PRIORITY_CACHEMISS

No information on the view is stored in the registry, so the default view for folders of this type should be used.



#### VIEW_PRIORITY_INHERIT

The view from the previous window should be inherited.



#### VIEW_PRIORITY_SHELLEXT_ASBACKUP

If the classic view is operative, the inherited view should be used.



#### VIEW_PRIORITY_DESPERATE

The last known good view supported by the window should be used.



#### VIEW_PRIORITY_NONE

No view is available at this point.