---
UID: NF:vswriter.IVssComponentEx.GetPostSnapshotFailureMsg
title: IVssComponentEx::GetPostSnapshotFailureMsg (vswriter.h)
description: Returns the PostSnapshot failure message string that a writer has set for a given component.
helpviewer_keywords: ["GetPostSnapshotFailureMsg","GetPostSnapshotFailureMsg method","GetPostSnapshotFailureMsg method","IVssComponentEx interface","IVssComponentEx interface","GetPostSnapshotFailureMsg method","IVssComponentEx.GetPostSnapshotFailureMsg","IVssComponentEx::GetPostSnapshotFailureMsg","base.ivsscomponentex_getpostsnapshotfailuremsg","vswriter/IVssComponentEx::GetPostSnapshotFailureMsg"]
old-location: base\ivsscomponentex_getpostsnapshotfailuremsg.htm
tech.root: base
ms.assetid: 51f96d3e-c783-42f4-9e04-94bf3a6b7c09
ms.date: 12/05/2018
ms.keywords: GetPostSnapshotFailureMsg, GetPostSnapshotFailureMsg method, GetPostSnapshotFailureMsg method,IVssComponentEx interface, IVssComponentEx interface,GetPostSnapshotFailureMsg method, IVssComponentEx.GetPostSnapshotFailureMsg, IVssComponentEx::GetPostSnapshotFailureMsg, base.ivsscomponentex_getpostsnapshotfailuremsg, vswriter/IVssComponentEx::GetPostSnapshotFailureMsg
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
 - IVssComponentEx::GetPostSnapshotFailureMsg
 - vswriter/IVssComponentEx::GetPostSnapshotFailureMsg
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
 - IVssComponentEx.GetPostSnapshotFailureMsg
---

# IVssComponentEx::GetPostSnapshotFailureMsg


## -description

Returns the <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> failure message string that a writer has  set for a given component.

Both writers and requesters can call this method. Writers should call this method after the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a> asynchronous operation has completed.

## -parameters

### -param pbstrFailureMsg [out]

A pointer to a null-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> 
      event.

## -returns

The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The failure message was successfully obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No <a href="/windows/desktop/VSS/vssgloss-p">PostSnapshot</a> failure message was set for the component.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
</table>

## -remarks

The caller is responsible for freeing the string that  the <i>pbstrFailureMsg</i> parameter points to by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -see-also

<a href="/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostsnapshot">CVssWriter::OnPostSnapshot</a>



<a href="/windows/desktop/api/vswriter/nl-vswriter-ivsscomponentex">IVssComponentEx</a>



<a href="/windows/desktop/api/vswriter/nf-vswriter-ivsscomponentex-setpostsnapshotfailuremsg">IVssComponentEx::SetPostSnapshotFailureMsg</a>