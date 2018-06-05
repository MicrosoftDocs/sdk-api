---
UID: NF:vswriter.IVssComponentEx.SetPostSnapshotFailureMsg
title: IVssComponentEx::SetPostSnapshotFailureMsg
author: windows-sdk-content
description: Sets a PostSnapshot failure message string for a component.
old-location: base\ivsscomponentex_setpostsnapshotfailuremsg.htm
old-project: VSS
ms.assetid: 7cf4e512-d557-4187-b489-5cca76c0560f
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IVssComponentEx interface,SetPostSnapshotFailureMsg method, IVssComponentEx.SetPostSnapshotFailureMsg, IVssComponentEx::SetPostSnapshotFailureMsg, SetPostSnapshotFailureMsg, SetPostSnapshotFailureMsg method, SetPostSnapshotFailureMsg method,IVssComponentEx interface, base.ivsscomponentex_setpostsnapshotfailuremsg, vswriter/IVssComponentEx::SetPostSnapshotFailureMsg
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssComponentEx.SetPostSnapshotFailureMsg
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssComponentEx::SetPostSnapshotFailureMsg


## -description


Sets a <a href="vssgloss_p.htm">PostSnapshot</a> failure message string for a component.

This method can only be called by a writer's <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a> method.


## -parameters




### -param wszFailureMsg [in]

The address of a caller-allocated <b>NULL</b>-terminated wide character string containing the failure message that describes an error that occurred 
      while processing a <a href="vssgloss_p.htm">PostSnapshot</a> 
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
The failure message was successfully set.

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
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_BAD_STATE</b></dt>
</dl>
</td>
<td width="60%">
This method was not called by a writer's <a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a> method.

</td>
</tr>
</table>
 




## -remarks



The failure message that is set by 
<b>SetPostSnapshotFailureMsg</b> applies to all files in the component and any subcomponents.




## -see-also




<a href="https://msdn.microsoft.com/d97d4246-882e-49c3-a214-d8d3887c1508">CVssWriter::OnPostSnapshot</a>



<a href="https://msdn.microsoft.com/b11f65b0-2de2-478b-88b6-4696a8da2419">IVssComponentEx</a>



<a href="https://msdn.microsoft.com/51f96d3e-c783-42f4-9e04-94bf3a6b7c09">IVssComponentEx::GetPostSnapshotFailureMsg</a>
 

 

