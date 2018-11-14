---
UID: NF:vswriter.IVssComponentEx.GetPostSnapshotFailureMsg
title: IVssComponentEx::GetPostSnapshotFailureMsg
author: windows-sdk-content
description: Returns the PostSnapshot failure message string that a writer has set for a given component.
old-location: base\ivsscomponentex_getpostsnapshotfailuremsg.htm
tech.root: VSS
ms.assetid: 51f96d3e-c783-42f4-9e04-94bf3a6b7c09
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPostSnapshotFailureMsg, GetPostSnapshotFailureMsg method, GetPostSnapshotFailureMsg method,IVssComponentEx interface, IVssComponentEx interface,GetPostSnapshotFailureMsg method, IVssComponentEx.GetPostSnapshotFailureMsg, IVssComponentEx::GetPostSnapshotFailureMsg, base.ivsscomponentex_getpostsnapshotfailuremsg, vswriter/IVssComponentEx::GetPostSnapshotFailureMsg
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IVssComponentEx.GetPostSnapshotFailureMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- vswriter.h
: 
- IVssComponentEx.GetPostSnapshotFailureMsg
: 
---

# IVssComponentEx::GetPostSnapshotFailureMsg


## -description


Returns the <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> failure message string that a writer has  set for a given component.

Both writers and requesters can call this method. Writers should call this method after the <a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a> asynchronous operation has completed.


## -parameters




### -param pbstrFailureMsg [out]

A pointer to a null-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> 
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
No <a href="https://msdn.microsoft.com/en-us/library/Aa384664(v=VS.85).aspx">PostSnapshot</a> failure message was set for the component.

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



The caller is responsible for freeing the string that  the <i>pbstrFailureMsg</i> parameter points to by calling the <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/7cf4e512-d557-4187-b489-5cca76c0560f">IVssComponentEx::SetPostSnapshotFailureMsg</a>
 

 

