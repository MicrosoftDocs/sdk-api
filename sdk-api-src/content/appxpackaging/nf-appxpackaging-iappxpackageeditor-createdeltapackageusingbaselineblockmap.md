---
UID: NF:appxpackaging.IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap
title: IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap method
author: windows-driver-content
description: Creates a delta package from the differences in the updated package and the baseline block map.
old-location: appxpkg\iappxpackageeditor_createdeltapackageusingbaselineblockmap.htm
old-project: appxpkg
ms.assetid: 33D1CEBA-A7F4-4506-B467-3610A3737B87
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management], CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management], IAppxPackageEditor interface, CreateDeltaPackageUsingBaselineBlockMap,IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap, IAppxPackageEditor, IAppxPackageEditor interface [App packaging and management], CreateDeltaPackageUsingBaselineBlockMap method, IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap, appxpackaging/IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap, appxpkg.iappxpackageeditor_createdeltapackageusingbaselineblockmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap method


## -description


Creates a delta package from the differences in the updated package and the baseline block map.


## -parameters




### -param updatedPackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the updated app package.


### -param baselineBlockMapStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the baseline block map.


### -param baselinePackageFullName [in]

The full name of the baseline app package.


### -param deltaPackageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of the delta (difference) app package.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/37D9494A-A5C0-4ABA-99BC-7F9B10E8D06C">IAppxPackageEditor</a>
 

 

