---
UID: NF:appxpackaging.IAppxContentGroupFilesEnumerator.GetCurrent
title: IAppxContentGroupFilesEnumerator::GetCurrent (appxpackaging.h)
description: Gets the file from the content group at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxContentGroupFilesEnumerator interface","IAppxContentGroupFilesEnumerator interface [App packaging and management]","GetCurrent method","IAppxContentGroupFilesEnumerator.GetCurrent","IAppxContentGroupFilesEnumerator::GetCurrent","appxpackaging/IAppxContentGroupFilesEnumerator::GetCurrent","appxpkg.iappxcontentgroupfilesenumerator__getcurrent"]
old-location: appxpkg\iappxcontentgroupfilesenumerator__getcurrent.htm
tech.root: appxpkg
ms.assetid: B8BD3A9A-5330-4328-9FFD-69BF07CA93C7
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxContentGroupFilesEnumerator interface, IAppxContentGroupFilesEnumerator interface [App packaging and management],GetCurrent method, IAppxContentGroupFilesEnumerator.GetCurrent, IAppxContentGroupFilesEnumerator::GetCurrent, appxpackaging/IAppxContentGroupFilesEnumerator::GetCurrent, appxpkg.iappxcontentgroupfilesenumerator__getcurrent
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IAppxContentGroupFilesEnumerator::GetCurrent
 - appxpackaging/IAppxContentGroupFilesEnumerator::GetCurrent
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
 - IAppxContentGroupFilesEnumerator.GetCurrent
---

# IAppxContentGroupFilesEnumerator::GetCurrent


## -description

Gets the file from the content group at the current position of the enumerator.

## -parameters

### -param file [out, retval]

The file at the position of the enumerator.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/appxpackaging/nn-appxpackaging-iappxcontentgroupfilesenumerator">IAppxContentGroupFilesEnumerator</a>

