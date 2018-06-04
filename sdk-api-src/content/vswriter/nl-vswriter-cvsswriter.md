---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
    <a href="https://msdn.microsoft.com/a427ebbd-b7c4-46ba-ba16-dd601b1f956e">CVssWriter::Initialize</a> and then call 
    <a href="https://msdn.microsoft.com/ab9520c9-bd6b-4c81-87fc-f5cda6ee9c94">CVssWriter::Subscribe</a>.

A writer terminates its participation by calling 
    <a href="https://msdn.microsoft.com/b2bb68d1-7beb-4ba1-b16d-6314ac3f4a3d">CVssWriter::Unsubscribe</a>.

The <b>CVssWriter</b> base class is responsible for the life cycle 
    of interfaces passed to event handlers. This includes the following:
<ul>
<li>The instance of the <a href="https://msdn.microsoft.com/e8ff2491-014c-43c7-bdce-99ed3b408605">IVssWriterComponents</a> 
     interface passed to:
     
<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>



<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>



<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>



<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>



<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>


</li>
<li>The instance of the 
     <a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a> interface passed to 
     <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriter::OnIdentify</a>.</li>
</ul><b xmlns:loc="http://microsoft.com/wdcml/l10n">CVssWriter</b> has these types of members:

