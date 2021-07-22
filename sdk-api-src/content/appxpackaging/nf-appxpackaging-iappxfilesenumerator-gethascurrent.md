---
UID: NF:appxpackaging.IAppxFilesEnumerator.GetHasCurrent
title: IAppxFilesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a payload file at the current position of the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxFilesEnumerator interface","IAppxFilesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxFilesEnumerator.GetHasCurrent","IAppxFilesEnumerator::GetHasCurrent","appxpackaging/IAppxFilesEnumerator::GetHasCurrent","appxpkg.iappxfilesenumerator_gethascurrent"]
old-location: appxpkg\iappxfilesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 4CC798E4-5FD2-45DE-BD3A-0B036601BEDB
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxFilesEnumerator interface, IAppxFilesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxFilesEnumerator.GetHasCurrent, IAppxFilesEnumerator::GetHasCurrent, appxpackaging/IAppxFilesEnumerator::GetHasCurrent, appxpkg.iappxfilesenumerator_gethascurrent
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxFilesEnumerator::GetHasCurrent
 - appxpackaging/IAppxFilesEnumerator::GetHasCurrent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxFilesEnumerator.GetHasCurrent
---

# IAppxFilesEnumerator::GetHasCurrent


## -description

Determines whether there is a payload file at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the current position references a payload file; <b>FALSE</b> if the enumerator has passed the end of the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxfilesenumerator">IAppxFilesEnumerator</a>