---
UID: NF:msctf.ITfContext.CreateRangeBackup
title: ITfContext::CreateRangeBackup
author: windows-sdk-content
description: ITfContext::CreateRangeBackup method
old-location: tsf\itfcontext_createrangebackup.htm
old-project: TSF
ms.assetid: c3b52170-af1b-407b-9160-1265ae3c9afc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateRangeBackup, CreateRangeBackup method [Text Services Framework], CreateRangeBackup method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],CreateRangeBackup method, ITfContext.CreateRangeBackup, ITfContext::CreateRangeBackup, _tsf_itfcontext_createrangebackup_ref, msctf/ITfContext::CreateRangeBackup, tsf.itfcontext_createrangebackup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContext.CreateRangeBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContext::CreateRangeBackup


## -description




## -parameters




### -param ec [in]

Contains an edit cookie that identifies the edit session. This is the value passed to <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


### -param pRange [in]

Pointer to the <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> object to be backed up.


### -param ppBackup [out]

Pointer to an <a href="https://msdn.microsoft.com/f98cd8d0-7033-4bd2-94a1-1a75913c2647">ITfRangeBackup</a> interface pointer that receives the backup of <i>pRange</i>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



This method creates a copy of the range that it can use to restore the data in <a href="https://msdn.microsoft.com/bb168504-34c0-4d30-826e-61926fd10a2a">ITfRangeBackup::Restore</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>



<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="https://msdn.microsoft.com/f98cd8d0-7033-4bd2-94a1-1a75913c2647">ITfRangeBackup
      </a>



<a href="https://msdn.microsoft.com/bb168504-34c0-4d30-826e-61926fd10a2a">ITfRangeBackup::Restore
      </a>



<a href="ranges.htm">Ranges: Clones and Backups</a>
 

 

