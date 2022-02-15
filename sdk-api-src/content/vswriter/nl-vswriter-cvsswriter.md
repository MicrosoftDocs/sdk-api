---
UID: NL:vswriter.CVssWriter
title: CVssWriter (vswriter.h)
description: The CVssWriter class is an abstract base class that defines the interface by which a writer synchronizes its state with VSS and other writers.
helpviewer_keywords: ["CVssWriter","CVssWriter class [VSS]","CVssWriter class [VSS]","described","_win32_cvsswriter","base.cvsswriter","vswriter/CVssWriter"]
old-location: base\cvsswriter.htm
tech.root: base
ms.assetid: 5d54c966-86ad-41af-82be-8a182b3d203a
ms.date: 12/05/2018
ms.keywords: CVssWriter, CVssWriter class [VSS], CVssWriter class [VSS],described, _win32_cvsswriter, base.cvsswriter, vswriter/CVssWriter
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - CVssWriter
 - vswriter/CVssWriter
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
 - CVssWriter
---

# CVssWriter class


## -description

The <b>CVssWriter</b> class is an abstract base class that defines 
    the interface by which a writer synchronizes its state with VSS and other writers.

Every writer must instantiate an object derived from 
    <b>CVssWriter</b>.

Objects derived from <b>CVssWriter</b> must supply implementations 
    for all of the <b>CVssWriter</b>'s pure virtual methods.

A writer can override one or all of <b>CVssWriter</b>'s virtual 
    methods.

To participate in VSS, a writer must first call 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize">CVssWriter::Initialize</a> and then call 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-subscribe">CVssWriter::Subscribe</a>.

A writer terminates its participation by calling 
    <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-unsubscribe">CVssWriter::Unsubscribe</a>.

The <b>CVssWriter</b> base class is responsible for the life cycle 
    of interfaces passed to event handlers. This includes the following:
<ul>
<li>The instance of the <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsswritercomponents">IVssWriterComponents</a> 
     interface passed to:
     
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>


</li>
<li>The instance of the 
     <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscreatewritermetadata">IVssCreateWriterMetadata</a> interface passed to 
     <a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onidentify">CVssWriter::OnIdentify</a>.</li>
</ul><b>CVssWriter</b> has these types of members: