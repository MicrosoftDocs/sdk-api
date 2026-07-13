---
UID: NF:shlobj.IFileViewerA.ShowInitialize
title: IFileViewerA::ShowInitialize
description: Allows a file viewer to determine whether it can display a file. (ANSI)
helpviewer_keywords: ["IFileViewerA::ShowInitialize"]
tech.root: shell
ms.assetid: 28f7deb9-09aa-4041-ac6a-3956fdc59191
ms.date: 01/30/2019
ms.keywords: IFileViewerA::ShowInitialize
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: shlobj.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - IFileViewerA::ShowInitialize
 - shlobj/IFileViewerA::ShowInitialize
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - IFileViewerA::ShowInitialize
---

## -description

Allows a file viewer to determine whether it can display a file and, if it can, to perform initialization operations before showing the file.

## -parameters

### -param lpfsi

A pointer to an [IFileViewerSite](nn-shlobj-ifileviewersite.md) interface. A file viewer uses this interface to retrieve the handle to the current pinned window or to specify a new pinned window.

## -returns

The Shell calls this method before the [Show](nf-shlobj-ifileviewera-show.md) method. The Shell specifies the name of the file to display by calling the file viewer's [IPersistFile::Load](/windows/desktop/api/objidl/nf-objidl-ipersistfile-load) method.

## -remarks

## -see-also
