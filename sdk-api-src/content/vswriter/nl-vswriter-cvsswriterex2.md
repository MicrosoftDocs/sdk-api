---
UID: NL:vswriter.CVssWriterEx2
title: CVssWriterEx2
author: windows-sdk-content
description: The CVssWriterEx2 class is an abstract base class that defines the interface by which a writer synchronizes its state with VSS and other writers.
old-location: base\cvsswriterex2.htm
tech.root: VSS
ms.assetid: 13cdeae3-dece-42ae-8bff-037ee3e4cec4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CVssWriterEx2, CVssWriterEx2 class, CVssWriterEx2 class,described, base.cvsswriterex2, vswriter/CVssWriterEx2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - CVssWriterEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CVssWriterEx2 class


## -description


The <b>CVssWriterEx2</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers.

The <b>CVssWriterEx2</b> class inherits the methods of the <a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a> class.

Every writer must create an instance of the  
    <b>CVssWriterEx2</b>, <a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a>, or <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>  class.

Objects that are derived from <b>CVssWriterEx2</b> must supply implementations 
    for all of the pure virtual methods of the <a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> classes.

A writer can override any or all of  the virtual 
    methods of <a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a> and <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>. However, a writer can override the <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">OnIdentify</a> or <a href="https://msdn.microsoft.com/4cb3b8f6-f702-4fba-a3cc-af84897cfd82">OnIdentifyEx</a> method, but not both.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CVssWriterEx2</b> has these types of members:


## -see-also




<a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a>



<a href="https://msdn.microsoft.com/29820c1d-2add-402d-a9ca-9e8674d85f7f">CVssWriterEx</a>
 

 

