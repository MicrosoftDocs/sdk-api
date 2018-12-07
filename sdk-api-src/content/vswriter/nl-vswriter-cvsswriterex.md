---
UID: NL:vswriter.CVssWriterEx
title: CVssWriterEx
author: windows-sdk-content
description: The CVssWriterEx class is an abstract base class that defines the interface by which a writer synchronizes its state with VSS and other writers.
old-location: base\cvsswriterex.htm
tech.root: vss
ms.assetid: 29820c1d-2add-402d-a9ca-9e8674d85f7f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CVssWriterEx, CVssWriterEx class, CVssWriterEx class,described, base.cvsswriterex, vswriter/CVssWriterEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - CVssWriterEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriterEx class


## -description


The <b>CVssWriterEx</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers. 

The <b>CVssWriterEx</b> class inherits the methods of the <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> class.

Every writer must create an instance of the  
    <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> or <b>CVssWriterEx</b> class.

Objects that are derived from <b>CVssWriterEx</b> must supply implementations 
    for all of the pure virtual methods of both the <b>CVssWriterEx</b> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> classes.

A writer can override any or all of  the virtual 
    methods of <b>CVssWriterEx</b> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>. However, a writer can override the <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">OnIdentify</a> or <a href="https://msdn.microsoft.com/4cb3b8f6-f702-4fba-a3cc-af84897cfd82">OnIdentifyEx</a> method, but not both.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CVssWriterEx</b> has these types of members:


## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>
 

 

