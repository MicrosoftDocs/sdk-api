---
UID: NF:appxpackaging.IAppxBlockMapFilesEnumerator.GetHasCurrent
title: IAppxBlockMapFilesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a file at the current position of the enumerator. (IAppxBlockMapFilesEnumerator.GetHasCurrent)
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxBlockMapFilesEnumerator interface","IAppxBlockMapFilesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxBlockMapFilesEnumerator.GetHasCurrent","IAppxBlockMapFilesEnumerator::GetHasCurrent","appxpackaging/IAppxBlockMapFilesEnumerator::GetHasCurrent","appxpkg.iappxblockmapfilesenumerator_gethascurrent"]
old-location: appxpkg\iappxblockmapfilesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: B0021CBC-9A3F-4D2D-8898-FE797396B312
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxBlockMapFilesEnumerator interface, IAppxBlockMapFilesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxBlockMapFilesEnumerator.GetHasCurrent, IAppxBlockMapFilesEnumerator::GetHasCurrent, appxpackaging/IAppxBlockMapFilesEnumerator::GetHasCurrent, appxpkg.iappxblockmapfilesenumerator_gethascurrent
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
 - IAppxBlockMapFilesEnumerator::GetHasCurrent
 - appxpackaging/IAppxBlockMapFilesEnumerator::GetHasCurrent
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
 - IAppxBlockMapFilesEnumerator.GetHasCurrent
---

# IAppxBlockMapFilesEnumerator::GetHasCurrent


## -description

Determines whether there is a file at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapfilesenumerator">IAppxBlockMapFilesEnumerator</a>
