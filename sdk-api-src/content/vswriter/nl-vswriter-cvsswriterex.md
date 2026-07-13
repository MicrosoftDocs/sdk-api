---
UID: NL:vswriter.CVssWriterEx
title: CVssWriterEx (vswriter.h)
description: The CVssWriterEx class is an abstract base class that defines the interface by which a writer synchronizes its state with VSS and other writers.
helpviewer_keywords: ["CVssWriterEx","CVssWriterEx class","CVssWriterEx class","described","base.cvsswriterex","vswriter/CVssWriterEx"]
old-location: base\cvsswriterex.htm
tech.root: base
ms.assetid: 29820c1d-2add-402d-a9ca-9e8674d85f7f
ms.date: 12/05/2018
ms.keywords: CVssWriterEx, CVssWriterEx class, CVssWriterEx class,described, base.cvsswriterex, vswriter/CVssWriterEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CVssWriterEx
 - vswriter/CVssWriterEx
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
 - CVssWriterEx
---

# CVssWriterEx class


## -description

The <b>CVssWriterEx</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers. 

The <b>CVssWriterEx</b> class inherits the methods of the <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> class.

Every writer must create an instance of the  
    <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> or <b>CVssWriterEx</b> class.

Objects that are derived from <b>CVssWriterEx</b> must supply implementations 
    for all of the pure virtual methods of both the <b>CVssWriterEx</b> and <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> classes.

A writer can override any or all of  the virtual 
    methods of <b>CVssWriterEx</b> and <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>. However, a writer can override the <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">OnIdentify</a> or <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriterex-onidentifyex">OnIdentifyEx</a> method, but not both.

<b>CVssWriterEx</b> has these types of members:

## -see-also

<a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a>