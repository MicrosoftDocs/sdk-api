---
UID: NL:vswriter.CVssWriterEx2
title: CVssWriterEx2 (vswriter.h)
description: The CVssWriterEx2 class is an abstract base class that defines the interface by which a writer synchronizes its state with VSS and other writers.
helpviewer_keywords: ["CVssWriterEx2","CVssWriterEx2 class","CVssWriterEx2 class","described","base.cvsswriterex2","vswriter/CVssWriterEx2"]
old-location: base\cvsswriterex2.htm
tech.root: base
ms.assetid: 13cdeae3-dece-42ae-8bff-037ee3e4cec4
ms.date: 12/05/2018
ms.keywords: CVssWriterEx2, CVssWriterEx2 class, CVssWriterEx2 class,described, base.cvsswriterex2, vswriter/CVssWriterEx2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriterEx2
 - vswriter/CVssWriterEx2
dev_langs:
 - c++
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
---

# CVssWriterEx2 class


## -description

The <b>CVssWriterEx2</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers.

The <b>CVssWriterEx2</b> class inherits the methods of the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> class.

Every writer must create an instance of the  
    <b>CVssWriterEx2</b>, <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>, or <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>  class.

Objects that are derived from <b>CVssWriterEx2</b> must supply implementations 
    for all of the pure virtual methods of the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> and <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> classes.

A writer can override any or all of  the virtual 
    methods of <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a> and <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>. However, a writer can override the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">OnIdentify</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">OnIdentifyEx</a> method, but not both.

<b>CVssWriterEx2</b> has these types of members:

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriterex">CVssWriterEx</a>