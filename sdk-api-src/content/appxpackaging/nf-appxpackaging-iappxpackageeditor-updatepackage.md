---
UID: NF:appxpackaging.IAppxPackageEditor.UpdatePackage
title: IAppxPackageEditor::UpdatePackage (appxpackaging.h)
description: Updates an app package.
old-location: appxpkg\iappxpackageeditor_updatepackage.htm
tech.root: appxpkg
ms.assetid: 768D2997-A374-46FF-BA0D-14B266D3C83D
ms.date: 12/05/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdatePackage method, IAppxPackageEditor.UpdatePackage, IAppxPackageEditor::UpdatePackage, UpdatePackage, UpdatePackage method [App packaging and management], UpdatePackage method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdatePackage, appxpkg.iappxpackageeditor_updatepackage
ms.topic: method
f1_keywords:
- appxpackaging/IAppxPackageEditor.UpdatePackage
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- AppxPackaging.h
api_name:
- IAppxPackageEditor.UpdatePackage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxPackageEditor::UpdatePackage


## -description


Updates an app package.


## -parameters




### -param baselinePackageStream [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the baseline app package.


### -param deltaPackageStream [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the delta (difference) app package.


### -param updateOption [in]

The update options.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackageeditor">IAppxPackageEditor</a>
 

 

