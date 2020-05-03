---
UID: NF:shlobj.IFileViewerW.ShowInitialize
title: IFileViewerW::ShowInitialize
description: Allows a file viewer to determine whether it can display a file.helpviewer_keywords: ["IFileViewerW::ShowInitialize"]
tech.root: shell
ms.assetid: 28f7deb9-09aa-4041-ac6a-3956fdc59191
ms.date: 01/30/19
ms.keywords: IFileViewerW::ShowInitialize
f1_keywords:
- shlobj/IFileViewerW::ShowInitialize
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- COM
api_location:
- shlobj.h
api_name:
- IFileViewerW::ShowInitialize
---

## -description

Allows a file viewer to determine whether it can display a file and, if it can, to perform initialization operations before showing the file.

## -parameters

### -param lpfsi

A pointer to an [IFileViewerSite](nn-shlobj-ifileviewersite.md) interface. A file viewer uses this interface to retrieve the handle to the current pinned window or to specify a new pinned window.

## -returns

The Shell calls this method before the [IFileViewerW::Show](C:\sdk-api\sdk-api-src\content\shlobj\nf-shlobj-ifileviewerw-show) method. The Shell specifies the name of the file to display by calling the file viewer's [IPersistFile::Load](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-load) method.

## -remarks

## -see-also

