---
UID: NL:vswriter.IVssWriterComponents
title: IVssWriterComponents (vswriter.h)
description: Contains methods used to obtain and modify component information.
helpviewer_keywords: ["IVssWriterComponents","IVssWriterComponents interface [VSS]","IVssWriterComponents interface [VSS]","described","_win32_ivsswritercomponents","base.ivsswritercomponents","vswriter/IVssWriterComponents"]
old-location: base\ivsswritercomponents.htm
tech.root: base
ms.assetid: e8ff2491-014c-43c7-bdce-99ed3b408605
ms.date: 12/05/2018
ms.keywords: IVssWriterComponents, IVssWriterComponents interface [VSS], IVssWriterComponents interface [VSS],described, _win32_ivsswritercomponents, base.ivsswritercomponents, vswriter/IVssWriterComponents
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
 - IVssWriterComponents
 - vswriter/IVssWriterComponents
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
 - IVssWriterComponents
---

# IVssWriterComponents class


## -description

The <b>IVssWriterComponents</b> interface is a C++ (not 
    COM) interface that contains methods used to obtain and modify component information (in the 
    form of <a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponent">IVssComponent</a> objects) associated with a given 
    writer but stored in a requester's Backup Components Document.

The <a href="/windows/desktop/api/vswriter/nl-vswriter-cvsswriter">CVssWriter</a> base class is responsible for passing an 
    instance of the <b>IVssWriterComponents</b> interface to 
    the following event handlers:
<ul>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpreparebackup">CVssWriter::OnPrepareBackup</a>
</li>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onbackupcomplete">CVssWriter::OnBackupComplete</a>
</li>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onprerestore">CVssWriter::OnPreRestore</a>
</li>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore">CVssWriter::OnPostRestore</a>
</li>
<li>
<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>
</li>
</ul>In addition, an instance of the 
    <a href="/windows/desktop/api/vsbackup/nl-vsbackup-ivsswritercomponentsext">IVssWriterComponentsExt</a> interface, which 
    implements a requester-side version of the 
    <b>IVssWriterComponents</b> interface, is returned by 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents">IVssBackupComponents::GetWriterComponents</a>.

<b>IVssWriterComponents</b> defines the following methods.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponent">GetComponent</a>
</td>
<td>Returns the components belonging to a given writer instance.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getcomponentcount">GetComponentCount</a>
</td>
<td>Returns the number of components belonging to a given writer instance.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsswritercomponents-getwriterinfo">GetWriterInfo</a>
</td>
<td>Returns the instance and class identifier of the writer responsible for the components.</td>
</tr>
</table>