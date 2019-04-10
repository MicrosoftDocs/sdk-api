---
UID: NF:pla.IConfigurationDataCollector.get_Files
title: IConfigurationDataCollector::get_Files (pla.h)
author: windows-sdk-content
description: Retrieves or sets the files to collect.
old-location: pla\iconfigurationdatacollector_files.htm
tech.root: PLA
ms.assetid: ca495768-8f84-489b-8590-3ab7d031f0be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Files property [PLA], Files property [PLA],IConfigurationDataCollector interface, IConfigurationDataCollector interface [PLA],Files property, IConfigurationDataCollector.Files, IConfigurationDataCollector.get_Files, IConfigurationDataCollector::Files, IConfigurationDataCollector::get_Files, IConfigurationDataCollector::put_Files, base.iconfigurationdatacollector_files, get_Files, pla.iconfigurationdatacollector_files, pla/IConfigurationDataCollector::Files, pla/IConfigurationDataCollector::get_Files, pla/IConfigurationDataCollector::put_Files
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigurationDataCollector::get_Files


## -description


Retrieves or sets the files to collect.

This property is read/write.


## -parameters


## -remarks



You can  use the <a href="https://msdn.microsoft.com/20089bc0-8af4-48b4-85aa-51ab2e4bf5be">IConfigurationDataCollector::FileMaxCount</a>, <a href="https://msdn.microsoft.com/79a87a02-6e9e-4b21-b90f-59c600349ae0">IConfigurationDataCollector::FileMaxRecursiveDepth</a>, and <a href="https://msdn.microsoft.com/bcfe2b95-770d-4543-8f79-c5f1b55c5dec">IConfigurationDataCollector::FileMaxTotalSize</a> properties to limit the number of files that PLA collects.

PLA copies the files to the location specified in the <a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">IDataCollectorSet::LatestOutputLocation</a> property. If more than one file has the same name, PLA leaves the first file name intact and appends _n (where n is a one-based serial number) to all subsequent files with the same name. You can use the XML report to determine the origin of each file.

The property performs a depth-first search using the  <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a> and  <a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a> functions. For example, assuming the following directory structure:

<pre class="syntax" xml:space="preserve"><code>MyDir
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
</code></pre>
PLA would collect the files in the following order (assuming that no limits were reached):

<pre class="syntax" xml:space="preserve"><code>q.txt
s.txt
g.txt
h.txt
a.txt
b.txt
c.txt
y.txt
z.txt
m.txt
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a>



<a href="https://msdn.microsoft.com/20089bc0-8af4-48b4-85aa-51ab2e4bf5be">IConfigurationDataCollector::FileMaxCount</a>



<a href="https://msdn.microsoft.com/79a87a02-6e9e-4b21-b90f-59c600349ae0">IConfigurationDataCollector::FileMaxRecursiveDepth</a>



<a href="https://msdn.microsoft.com/bcfe2b95-770d-4543-8f79-c5f1b55c5dec">IConfigurationDataCollector::FileMaxTotalSize</a>
 

 

