---
UID: NF:shlobj.IFileViewerA.Show
title: IFileViewerA::Show
description: Displays a file. (ANSI)
helpviewer_keywords: ["IFileViewerA::Show"]
tech.root: shell
ms.assetid: 7555b40b-62c1-467a-b9d5-324fd1a7fd8e
ms.date: 01/30/2019
ms.keywords: IFileViewerA::Show
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
 - IFileViewerA::Show
 - shlobj/IFileViewerA::Show
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - shlobj.h
api_name:
 - IFileViewerA::Show
---

## -description

Displays a file. The Shell specifies the name of the file to display by calling the file viewer's [IPersistFile::Load](/windows/desktop/api/objidl/nf-objidl-ipersistfile-load) method.

## -parameters

### -param pvsi

A pointer to an [FVSHOWINFO](/windows/desktop/api/shlobj/ns-shlobj-fvshowinfo) structure to contain information that the file viewer uses to display the file. A file viewer can return information to the Shell by modifying the members of the structure.

## -returns

Returns S_OK if successful, or E_UNEXPECTED if the [ShowInitialize](nf-shlobj-ifileviewera-showinitialize.md) method was not called before **IFileViewerA::Show**.

## -remarks

## -see-also
