---
UID: NF:pla.IConfigurationDataCollector.get_Files
title: IConfigurationDataCollector::get_Files (pla.h)
description: Retrieves or sets the files to collect. (Get)
helpviewer_keywords: ["Files property [PLA]","Files property [PLA]","IConfigurationDataCollector interface","IConfigurationDataCollector interface [PLA]","Files property","IConfigurationDataCollector.Files","IConfigurationDataCollector.get_Files","IConfigurationDataCollector::Files","IConfigurationDataCollector::get_Files","IConfigurationDataCollector::put_Files","base.iconfigurationdatacollector_files","get_Files","pla.iconfigurationdatacollector_files","pla/IConfigurationDataCollector::Files","pla/IConfigurationDataCollector::get_Files","pla/IConfigurationDataCollector::put_Files"]
old-location: pla\iconfigurationdatacollector_files.htm
tech.root: PLA
ms.assetid: ca495768-8f84-489b-8590-3ab7d031f0be
ms.date: 12/05/2018
ms.keywords: Files property [PLA], Files property [PLA],IConfigurationDataCollector interface, IConfigurationDataCollector interface [PLA],Files property, IConfigurationDataCollector.Files, IConfigurationDataCollector.get_Files, IConfigurationDataCollector::Files, IConfigurationDataCollector::get_Files, IConfigurationDataCollector::put_Files, base.iconfigurationdatacollector_files, get_Files, pla.iconfigurationdatacollector_files, pla/IConfigurationDataCollector::Files, pla/IConfigurationDataCollector::get_Files, pla/IConfigurationDataCollector::put_Files
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConfigurationDataCollector::get_Files
 - pla/IConfigurationDataCollector::get_Files
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IConfigurationDataCollector.Files
 - IConfigurationDataCollector.get_Files
 - IConfigurationDataCollector.put_Files
---

# IConfigurationDataCollector::get_Files


## -description

Retrieves or sets the files to collect.

This property is read/write.

## -parameters

## -remarks

You can  use the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxcount">IConfigurationDataCollector::FileMaxCount</a>, <a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxrecursivedepth">IConfigurationDataCollector::FileMaxRecursiveDepth</a>, and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxtotalsize">IConfigurationDataCollector::FileMaxTotalSize</a> properties to limit the number of files that PLA collects.

PLA copies the files to the location specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_latestoutputlocation">IDataCollectorSet::LatestOutputLocation</a> property. If more than one file has the same name, PLA leaves the first file name intact and appends _n (where n is a one-based serial number) to all subsequent files with the same name. You can use the XML report to determine the origin of each file.

The property performs a depth-first search using the  <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> and  <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a> functions. For example, assuming the following directory structure:


``` syntax
MyDir
    Subdir1
        Subdir1.1
            a.txt
            b.txt
        Subdir1.2
            c.txt
        g.txt  (folder in Subdir1)
        h.txt  (folder in Subdir1)
    Subdir 2
        subdir2.1
            y.txt
            z.txt
            subdir2.1.1
                m.txt
    q.txt  (folder in MyDir)
    s.txt  (folder in MyDir)

```

PLA would collect the files in the following order (assuming that no limits were reached):


``` syntax
q.txt
s.txt
g.txt
h.txt
a.txt
b.txt
c.txt
y.txt
z.txt
m.txt

```


## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxcount">IConfigurationDataCollector::FileMaxCount</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxrecursivedepth">IConfigurationDataCollector::FileMaxRecursiveDepth</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-iconfigurationdatacollector-get_filemaxtotalsize">IConfigurationDataCollector::FileMaxTotalSize</a>
