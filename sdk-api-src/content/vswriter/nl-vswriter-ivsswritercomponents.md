---
UID: NL:vswriter.IVssWriterComponents
title: IVssWriterComponents
author: windows-sdk-content
description: Contains methods used to obtain and modify component information.
old-location: base\ivsswritercomponents.htm
tech.root: VSS
ms.assetid: e8ff2491-014c-43c7-bdce-99ed3b408605
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IVssWriterComponents, IVssWriterComponents interface [VSS], IVssWriterComponents interface [VSS],described, _win32_ivsswritercomponents, base.ivsswritercomponents, vswriter/IVssWriterComponents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssWriterComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssWriterComponents class


## -description


The <b>IVssWriterComponents</b> interface is a C++ (not 
    COM) interface that contains methods used to obtain and modify component information (in the 
    form of <a href="https://msdn.microsoft.com/c686a424-b0b9-4efc-8dc6-b92193de2a5d">IVssComponent</a> objects) associated with a given 
    writer but stored in a requester's Backup Components Document.

The <a href="https://msdn.microsoft.com/5d54c966-86ad-41af-82be-8a182b3d203a">CVssWriter</a> base class is responsible for passing an 
    instance of the <b>IVssWriterComponents</b> interface to 
    the following event handlers:
<ul>
<li>
<a href="https://msdn.microsoft.com/4e88d92b-48f3-42f9-bf66-61337a745902">CVssWriter::OnPrepareBackup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/77d0621d-81bd-4d53-8e5d-f5d3bfd86013">CVssWriter::OnBackupComplete</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f4a6168-4102-4790-81d6-d195a440471f">CVssWriter::OnPreRestore</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ad07753c-1592-4fc8-9899-a73e798c158c">CVssWriter::OnPostRestore</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>
</li>
</ul>In addition, an instance of the 
    <a href="https://msdn.microsoft.com/29772c1f-1cc4-4ee7-8e1d-f1a6cbebf470">IVssWriterComponentsExt</a> interface, which 
    implements a requester-side version of the 
    <b>IVssWriterComponents</b> interface, is returned by 
    <a href="https://msdn.microsoft.com/b99e7e41-1c88-462c-b6d8-734f7a6e24d4">IVssBackupComponents::GetWriterComponents</a>.

<b>IVssWriterComponents</b> defines the following methods.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ee816d83-31f3-47ff-b581-cc4dcd878f22">GetComponent</a>
</td>
<td>Returns the components belonging to a given writer instance.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ec89438f-4811-42f7-bda0-6df6d1b98f18">GetComponentCount</a>
</td>
<td>Returns the number of components belonging to a given writer instance.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/22a539ac-1440-4fe9-b68e-feec97cab6c8">GetWriterInfo</a>
</td>
<td>Returns the instance and class identifier of the writer responsible for the components.</td>
</tr>
</table>
 



