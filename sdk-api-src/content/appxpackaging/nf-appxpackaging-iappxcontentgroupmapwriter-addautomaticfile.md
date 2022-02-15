---
UID: NF:appxpackaging.IAppxContentGroupMapWriter.AddAutomaticFile
title: IAppxContentGroupMapWriter::AddAutomaticFile (appxpackaging.h)
description: Adds files to an automatic content group in a content group map.
helpviewer_keywords: ["AddAutomaticFile","AddAutomaticFile method [App packaging and management]","AddAutomaticFile method [App packaging and management]","IAppxContentGroupMapWriter interface","IAppxContentGroupMapWriter interface [App packaging and management]","AddAutomaticFile method","IAppxContentGroupMapWriter.AddAutomaticFile","IAppxContentGroupMapWriter::AddAutomaticFile","appxpackaging/IAppxContentGroupMapWriter::AddAutomaticFile","appxpkg.iappxcontentgroupmapwriter_addautomaticfile"]
old-location: appxpkg\iappxcontentgroupmapwriter_addautomaticfile.htm
tech.root: appxpkg
ms.assetid: 73F03332-8427-4470-9001-5EA9481BB05E
ms.date: 12/05/2018
ms.keywords: AddAutomaticFile, AddAutomaticFile method [App packaging and management], AddAutomaticFile method [App packaging and management],IAppxContentGroupMapWriter interface, IAppxContentGroupMapWriter interface [App packaging and management],AddAutomaticFile method, IAppxContentGroupMapWriter.AddAutomaticFile, IAppxContentGroupMapWriter::AddAutomaticFile, appxpackaging/IAppxContentGroupMapWriter::AddAutomaticFile, appxpkg.iappxcontentgroupmapwriter_addautomaticfile
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
 - IAppxContentGroupMapWriter::AddAutomaticFile
 - appxpackaging/IAppxContentGroupMapWriter::AddAutomaticFile
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
 - IAppxContentGroupMapWriter.AddAutomaticFile
---

# IAppxContentGroupMapWriter::AddAutomaticFile


## -description

Adds files to an automatic content group in a content group map.

## -parameters

### -param fileName [in]

The name of the file to be added to the automatic content group.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxcontentgroupmapwriter">IAppxContentGroupMapWriter</a>